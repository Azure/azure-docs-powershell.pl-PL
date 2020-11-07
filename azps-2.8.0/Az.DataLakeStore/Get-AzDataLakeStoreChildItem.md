---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 828418095c7e77a7ee484d00e9d4d3f6f4a9927b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705826"
---
# <span data-ttu-id="d5cfa-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="d5cfa-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="d5cfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="d5cfa-103">Pobiera listę elementów w folderze w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="d5cfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5cfa-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5cfa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5cfa-105">DESCRIPTION</span></span>
<span data-ttu-id="d5cfa-106">Polecenie cmdlet **Get-AzDataLakeStoreChildItem** pobiera listę elementów w folderze w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="d5cfa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5cfa-107">EXAMPLES</span></span>

### <span data-ttu-id="d5cfa-108">Przykład 1. Pobieranie elementów podrzędnych folderu</span><span class="sxs-lookup"><span data-stu-id="d5cfa-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="d5cfa-109">To polecenie pobiera elementy podrzędne folderu Moje pliki.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="d5cfa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5cfa-110">PARAMETERS</span></span>

### <span data-ttu-id="d5cfa-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="d5cfa-111">-Account</span></span>
<span data-ttu-id="d5cfa-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d5cfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5cfa-113">-DefaultProfile</span></span>
<span data-ttu-id="d5cfa-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5cfa-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d5cfa-115">-Path</span></span>
<span data-ttu-id="d5cfa-116">Określa ścieżkę folderu w usłudze Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="d5cfa-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d5cfa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5cfa-117">CommonParameters</span></span>
<span data-ttu-id="d5cfa-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5cfa-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5cfa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5cfa-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5cfa-120">INPUTS</span></span>

### <span data-ttu-id="d5cfa-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d5cfa-121">System.String</span></span>

### <span data-ttu-id="d5cfa-122">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d5cfa-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="d5cfa-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5cfa-123">OUTPUTS</span></span>

### <span data-ttu-id="d5cfa-124">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d5cfa-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="d5cfa-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5cfa-125">NOTES</span></span>

## <span data-ttu-id="d5cfa-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5cfa-126">RELATED LINKS</span></span>