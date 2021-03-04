---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: e27fde6a25fc512b898ded7d4f087ab7b344d293
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957297"
---
# <span data-ttu-id="d3056-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="d3056-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="d3056-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3056-102">SYNOPSIS</span></span>
<span data-ttu-id="d3056-103">Pobiera listę elementów w folderze w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d3056-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="d3056-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3056-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3056-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3056-105">DESCRIPTION</span></span>
<span data-ttu-id="d3056-106">Polecenie **cmdlet Get-AzDataLakeStoreChildItem** pobiera listę elementów w folderze w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d3056-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="d3056-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3056-107">EXAMPLES</span></span>

### <span data-ttu-id="d3056-108">Przykład 1. Uzyskiwanie elementów podrzędnego folderu</span><span class="sxs-lookup"><span data-stu-id="d3056-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="d3056-109">To polecenie pobiera elementy podrzędne dla folderu MyFiles.</span><span class="sxs-lookup"><span data-stu-id="d3056-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="d3056-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3056-110">PARAMETERS</span></span>

### <span data-ttu-id="d3056-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="d3056-111">-Account</span></span>
<span data-ttu-id="d3056-112">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d3056-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d3056-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3056-113">-DefaultProfile</span></span>
<span data-ttu-id="d3056-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3056-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3056-115">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="d3056-115">-Path</span></span>
<span data-ttu-id="d3056-116">Określa ścieżkę folderu do magazynu Data Lake Store rozpoczynającą się od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="d3056-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d3056-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3056-117">CommonParameters</span></span>
<span data-ttu-id="d3056-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3056-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3056-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3056-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3056-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3056-120">INPUTS</span></span>

### <span data-ttu-id="d3056-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d3056-121">System.String</span></span>

### <span data-ttu-id="d3056-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d3056-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="d3056-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3056-123">OUTPUTS</span></span>

### <span data-ttu-id="d3056-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d3056-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="d3056-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3056-125">NOTES</span></span>

## <span data-ttu-id="d3056-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3056-126">RELATED LINKS</span></span>
