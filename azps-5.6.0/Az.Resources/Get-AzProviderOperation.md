---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 61e38afcccccd6a96e92983d24442740351320ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016042"
---
# <span data-ttu-id="3f079-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3f079-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="3f079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f079-102">SYNOPSIS</span></span>
<span data-ttu-id="3f079-103">Pobiera operacje dla dostawcy zasobów platformy Azure, które są zabezpieczane przy użyciu usługi Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="3f079-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="3f079-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3f079-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f079-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3f079-105">DESCRIPTION</span></span>
<span data-ttu-id="3f079-106">Ten Get-AzProviderOperation uzyskuje dostęp do operacji ujawnionych przez dostawców zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3f079-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="3f079-107">Operacje można tworzyć w celu utworzenia ról niestandardowych w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="3f079-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="3f079-108">Polecenie przyjmuje jako dane wejściowe ciąg wyszukiwania operacji (z możliwymi znakami wieloznacznych()), który określa szczegóły operacji *do wyświetlenia. Użyj Get-AzProviderOperation \* w celu uzyskania wszystkich operacji dla wszystkich dostawców zasobów platformy Azure. Użyj Get-AzProviderOperation Microsoft.Compute/,* aby uzyskać wszystkie operacje dostawcy zasobów Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="3f079-108">The command takes as input an operation search string (with possible wildcard(*) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="3f079-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3f079-109">EXAMPLES</span></span>

### <span data-ttu-id="3f079-110">Przykład 1. Uzyskiwanie wszystkich akcji dla wszystkich dostawców</span><span class="sxs-lookup"><span data-stu-id="3f079-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="3f079-111">Przykład 2. Uzyskiwanie akcji dla określonego dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="3f079-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="3f079-112">Przykład 3. Uzyskaj wszystkie akcje, które mogą być wykonywane na komputerach wirtualnych</span><span class="sxs-lookup"><span data-stu-id="3f079-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="3f079-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f079-113">PARAMETERS</span></span>

### <span data-ttu-id="3f079-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f079-114">-DefaultProfile</span></span>
<span data-ttu-id="3f079-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3f079-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f079-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="3f079-116">-OperationSearchString</span></span>
<span data-ttu-id="3f079-117">Ciąg wyszukiwania operacji (z możliwymi symbolami wieloznacznymi (\*) )</span><span class="sxs-lookup"><span data-stu-id="3f079-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f079-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f079-118">CommonParameters</span></span>
<span data-ttu-id="3f079-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f079-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f079-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f079-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f079-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f079-121">INPUTS</span></span>

### <span data-ttu-id="3f079-122">System.String</span><span class="sxs-lookup"><span data-stu-id="3f079-122">System.String</span></span>

## <span data-ttu-id="3f079-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f079-123">OUTPUTS</span></span>

### <span data-ttu-id="3f079-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3f079-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="3f079-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3f079-125">NOTES</span></span>
<span data-ttu-id="3f079-126">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="3f079-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3f079-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f079-127">RELATED LINKS</span></span>
