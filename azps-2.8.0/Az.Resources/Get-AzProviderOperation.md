---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bd0483cf03ac5cff224824cc41b3fab994006acb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873396"
---
# <span data-ttu-id="4c118-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="4c118-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="4c118-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c118-102">SYNOPSIS</span></span>
<span data-ttu-id="4c118-103">Pobiera operacje dla dostawcy zasobów platformy Azure, które są zabezpieczane przy użyciu usługi Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="4c118-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="4c118-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c118-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c118-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c118-105">DESCRIPTION</span></span>
<span data-ttu-id="4c118-106">Get-AzProviderOperation pobiera operacje udostępnione przez dostawców zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4c118-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="4c118-107">Operacje mogą być składane w celu utworzenia ról niestandardowych w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="4c118-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="4c118-108">Polecenie przyjmuje jako wartość wejściową ciąg wyszukiwania operacji (z możliwymi znakami wieloznacznymi) \*, który określa szczegóły operacji do wyświetlenia. Użyj Get-AzProviderOperation *, aby pobrać wszystkie operacje dla wszystkich dostawców zasobów platformy Azure. Użyj Get-AzProviderOperation Microsoft. COMPUTE/* , aby pobrać wszystkie operacje dotyczące dostawcy zasobów Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="4c118-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="4c118-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c118-109">EXAMPLES</span></span>

### <span data-ttu-id="4c118-110">Pobierz wszystkie akcje dla wszystkich dostawców</span><span class="sxs-lookup"><span data-stu-id="4c118-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="4c118-111">Uzyskiwanie akcji dla określonego dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="4c118-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="4c118-112">Uzyskiwanie wszystkich akcji, które można wykonywać na maszynach wirtualnych</span><span class="sxs-lookup"><span data-stu-id="4c118-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="4c118-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c118-113">PARAMETERS</span></span>

### <span data-ttu-id="4c118-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c118-114">-DefaultProfile</span></span>
<span data-ttu-id="4c118-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4c118-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c118-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="4c118-116">-OperationSearchString</span></span>
<span data-ttu-id="4c118-117">Ciąg wyszukiwania operacji (z możliwymi symbolami wieloznacznymi (\*))</span><span class="sxs-lookup"><span data-stu-id="4c118-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="4c118-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c118-118">CommonParameters</span></span>
<span data-ttu-id="4c118-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c118-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c118-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c118-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c118-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c118-121">INPUTS</span></span>

### <span data-ttu-id="4c118-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4c118-122">System.String</span></span>

## <span data-ttu-id="4c118-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c118-123">OUTPUTS</span></span>

### <span data-ttu-id="4c118-124">Microsoft. Azure. Commands. resources. models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="4c118-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="4c118-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c118-125">NOTES</span></span>
<span data-ttu-id="4c118-126">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="4c118-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="4c118-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c118-127">RELATED LINKS</span></span>
