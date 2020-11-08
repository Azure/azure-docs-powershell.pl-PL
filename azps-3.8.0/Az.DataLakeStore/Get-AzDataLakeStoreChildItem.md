---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 6123cacd35eb0a683ec2103ea00e2e06a2d80cd2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049470"
---
# <span data-ttu-id="2e785-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="2e785-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="2e785-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e785-102">SYNOPSIS</span></span>
<span data-ttu-id="2e785-103">Pobiera listę elementów w folderze w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2e785-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="2e785-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e785-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e785-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e785-105">DESCRIPTION</span></span>
<span data-ttu-id="2e785-106">Polecenie cmdlet **Get-AzDataLakeStoreChildItem** pobiera listę elementów w folderze w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2e785-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="2e785-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e785-107">EXAMPLES</span></span>

### <span data-ttu-id="2e785-108">Przykład 1. Pobieranie elementów podrzędnych folderu</span><span class="sxs-lookup"><span data-stu-id="2e785-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="2e785-109">To polecenie pobiera elementy podrzędne folderu Moje pliki.</span><span class="sxs-lookup"><span data-stu-id="2e785-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="2e785-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e785-110">PARAMETERS</span></span>

### <span data-ttu-id="2e785-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="2e785-111">-Account</span></span>
<span data-ttu-id="2e785-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2e785-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e785-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e785-113">-DefaultProfile</span></span>
<span data-ttu-id="2e785-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e785-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e785-115">-Path</span><span class="sxs-lookup"><span data-stu-id="2e785-115">-Path</span></span>
<span data-ttu-id="2e785-116">Określa ścieżkę folderu w usłudze Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="2e785-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e785-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e785-117">CommonParameters</span></span>
<span data-ttu-id="2e785-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e785-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e785-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e785-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e785-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e785-120">INPUTS</span></span>

### <span data-ttu-id="2e785-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2e785-121">System.String</span></span>

### <span data-ttu-id="2e785-122">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2e785-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="2e785-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e785-123">OUTPUTS</span></span>

### <span data-ttu-id="2e785-124">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2e785-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="2e785-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e785-125">NOTES</span></span>

## <span data-ttu-id="2e785-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e785-126">RELATED LINKS</span></span>
