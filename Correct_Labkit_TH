% Aim: to correct the labkit predicted tif stack for TH+ region.
file_path = 'D:\QMDownload\9\1\57C10.J7.mino.IR-day32-PAM-0023.tif';
file_path_out =  'D:\QMDownload\9\1\57C10.J7.mino.IR-day32-PAM-0023_corrected.tif';
info = imfinfo(file_path);
for i = 1:length(info)
    aSlice = imread(file_path,i);
    aSlice=imgaussfilt(aSlice,1.5)>0.25;
    aSlice=imdilate(aSlice,strel('square',5));
    aSlice=~bwareaopen(~aSlice,200);
    aSlice=imerode(aSlice,strel('square',5));
    if i==1
        imwrite(uint8(aSlice),file_path_out,'WriteMode','overwrite');
    else
        imwrite(uint8(aSlice),file_path_out,'WriteMode','append');
    end
end

