---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490509"
---
# <span data-ttu-id="b6d7f-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b6d7f-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="b6d7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d7f-103">Pobiera operacje dla dostawcy zasobów platformy Azure, które są zabezpieczane przy użyciu usługi Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b6d7f-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="b6d7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6d7f-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6d7f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6d7f-105">DESCRIPTION</span></span>
<span data-ttu-id="b6d7f-106">Get-AzProviderOperation pobiera operacje udostępnione przez dostawców zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6d7f-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="b6d7f-107">Operacje mogą być składane w celu utworzenia ról niestandardowych w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b6d7f-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="b6d7f-108">Polecenie przyjmuje jako wartość wejściową ciąg wyszukiwania operacji (z możliwymi znakami wieloznacznymi)\*, który określa szczegóły operacji do wyświetlenia. Użyj Get-AzProviderOperation *, aby pobrać wszystkie operacje dla wszystkich dostawców zasobów platformy Azure. Użyj Get-AzProviderOperation Microsoft. COMPUTE/* , aby pobrać wszystkie operacje dotyczące dostawcy zasobów Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="b6d7f-108">The command takes as input an operation search string (with possible wildcard(*) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="b6d7f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6d7f-109">EXAMPLES</span></span>

### <span data-ttu-id="b6d7f-110">Przykład 1: pobieranie wszystkich akcji dla wszystkich dostawców</span><span class="sxs-lookup"><span data-stu-id="b6d7f-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="b6d7f-111">Przykład 2: uzyskiwanie akcji dla określonego dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="b6d7f-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="b6d7f-112">Przykład 3: uzyskiwanie wszystkich akcji, które można wykonywać na maszynach wirtualnych</span><span class="sxs-lookup"><span data-stu-id="b6d7f-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="b6d7f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6d7f-113">PARAMETERS</span></span>

### <span data-ttu-id="b6d7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d7f-114">-DefaultProfile</span></span>
<span data-ttu-id="b6d7f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b6d7f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6d7f-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="b6d7f-116">-OperationSearchString</span></span>
<span data-ttu-id="b6d7f-117">Ciąg wyszukiwania operacji (z możliwymi symbolami wieloznacznymi (\*))</span><span class="sxs-lookup"><span data-stu-id="b6d7f-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="b6d7f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d7f-118">CommonParameters</span></span>
<span data-ttu-id="b6d7f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6d7f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d7f-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6d7f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d7f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6d7f-121">INPUTS</span></span>

### <span data-ttu-id="b6d7f-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b6d7f-122">System.String</span></span>

## <span data-ttu-id="b6d7f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6d7f-123">OUTPUTS</span></span>

### <span data-ttu-id="b6d7f-124">Microsoft. Azure. Commands. resources. models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b6d7f-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="b6d7f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6d7f-125">NOTES</span></span>
<span data-ttu-id="b6d7f-126">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="b6d7f-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b6d7f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6d7f-127">RELATED LINKS</span></span>
