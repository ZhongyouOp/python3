##!/usr/bin/python3
# -*- coding: utf-8 -*-
# @Time    : 2022-6-21 16:51:55
# @Author  : zhongyou
# @Descr   : 将文件中的url提取出来


import argparse
import re


parser = argparse.ArgumentParser(description='test')
parser.add_argument('-f', help='读取txt')
parser.add_argument('-o', help='输出txt.')

args = parser.parse_args()


def read_txt(file, outfile):
    f = open(file)

    content = f.read()
    print(content.rstrip())
    result = re.findall(r'(https?://[^\s]+)', content)
    fo = open(outfile, "w")

    for i in result:
        print(i, file=fo)

    f.close()
    fo.close()


if __name__ == "__main__":
    read_txt(args.f, args.o)
