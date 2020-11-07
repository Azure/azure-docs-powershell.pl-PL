---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 21e1af2a36478f2e0b8e470660d0fbe2539a396e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892582"
---
# <span data-ttu-id="3709d-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3709d-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="3709d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3709d-102">SYNOPSIS</span></span>
<span data-ttu-id="3709d-103">Pobiera operacje dla dostawcy zasobów platformy Azure, które są zabezpieczane przy użyciu usługi Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="3709d-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="3709d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3709d-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3709d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3709d-105">DESCRIPTION</span></span>
<span data-ttu-id="3709d-106">Get-AzProviderOperation pobiera operacje udostępnione przez dostawców zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3709d-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="3709d-107">Operacje mogą być składane w celu utworzenia ról niestandardowych w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="3709d-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="3709d-108">Polecenie przyjmuje jako wartość wejściową ciąg wyszukiwania operacji (z możliwymi znakami wieloznacznymi) \*, który określa szczegóły operacji do wyświetlenia. Użyj Get-AzProviderOperation *, aby pobrać wszystkie operacje dla wszystkich dostawców zasobów platformy Azure. Użyj Get-AzProviderOperation Microsoft. COMPUTE/* , aby pobrać wszystkie operacje dotyczące dostawcy zasobów Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="3709d-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="3709d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3709d-109">EXAMPLES</span></span>

### <span data-ttu-id="3709d-110">Pobierz wszystkie akcje dla wszystkich dostawców</span><span class="sxs-lookup"><span data-stu-id="3709d-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="3709d-111">Uzyskiwanie akcji dla określonego dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="3709d-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="3709d-112">Uzyskiwanie wszystkich akcji, które można wykonywać na maszynach wirtualnych</span><span class="sxs-lookup"><span data-stu-id="3709d-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="3709d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3709d-113">PARAMETERS</span></span>

### <span data-ttu-id="3709d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3709d-114">-DefaultProfile</span></span>
<span data-ttu-id="3709d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3709d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3709d-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="3709d-116">-OperationSearchString</span></span>
<span data-ttu-id="3709d-117">Ciąg wyszukiwania operacji (z możliwymi symbolami wieloznacznymi (\*))</span><span class="sxs-lookup"><span data-stu-id="3709d-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="3709d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3709d-118">CommonParameters</span></span>
<span data-ttu-id="3709d-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3709d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3709d-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3709d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3709d-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3709d-121">INPUTS</span></span>

### <span data-ttu-id="3709d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="3709d-122">System.String</span></span>
<span data-ttu-id="3709d-123">Parametry: OperationSearchString (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3709d-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="3709d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3709d-124">OUTPUTS</span></span>

### <span data-ttu-id="3709d-125">Microsoft. Azure. Commands. resources. models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3709d-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="3709d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3709d-126">NOTES</span></span>
<span data-ttu-id="3709d-127">Słowa kluczowe: Azure, AZ, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="3709d-127">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3709d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3709d-128">RELATED LINKS</span></span>
