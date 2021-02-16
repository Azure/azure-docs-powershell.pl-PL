---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183195"
---
# <span data-ttu-id="2d829-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2d829-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="2d829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d829-102">SYNOPSIS</span></span>
<span data-ttu-id="2d829-103">Pobiera użycie zasobu magazynu bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2d829-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="2d829-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2d829-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d829-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2d829-105">DESCRIPTION</span></span>
<span data-ttu-id="2d829-106">Polecenie **cmdlet Get-AzStorageUsage** pobiera użycie zasobów dla magazynu platformy Azure dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2d829-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="2d829-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2d829-107">EXAMPLES</span></span>

### <span data-ttu-id="2d829-108">Przykład 1. Uzyskiwanie użycia zasobów magazynu dla określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="2d829-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="2d829-109">To polecenie pobiera użycie zasobów magazynu dla określonej lokalizacji w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2d829-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="2d829-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d829-110">PARAMETERS</span></span>

### <span data-ttu-id="2d829-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d829-111">-DefaultProfile</span></span>
<span data-ttu-id="2d829-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d829-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d829-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2d829-113">-Location</span></span>
<span data-ttu-id="2d829-114">Wskaż, aby uzyskać użycie zasobów magazynu w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2d829-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="2d829-115">Jeśli nie zostanie określona, zostanie jej użycie we wszystkich lokalizacjach w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2d829-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d829-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d829-116">CommonParameters</span></span>
<span data-ttu-id="2d829-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d829-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d829-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d829-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d829-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d829-119">INPUTS</span></span>

### <span data-ttu-id="2d829-120">System.String</span><span class="sxs-lookup"><span data-stu-id="2d829-120">System.String</span></span>

## <span data-ttu-id="2d829-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d829-121">OUTPUTS</span></span>

### <span data-ttu-id="2d829-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="2d829-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="2d829-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2d829-123">NOTES</span></span>

## <span data-ttu-id="2d829-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d829-124">RELATED LINKS</span></span>

[<span data-ttu-id="2d829-125">Polecenia cmdlet menedżera magazynowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2d829-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


