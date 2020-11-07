---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: 51229c966c0e4c8b0ec74c3c940037aca5081b15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718478"
---
# <span data-ttu-id="3c732-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3c732-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="3c732-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c732-102">SYNOPSIS</span></span>
<span data-ttu-id="3c732-103">Pobiera operacje dla dostawcy zasobów platformy Azure, które są zabezpieczane przy użyciu usługi Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="3c732-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c732-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c732-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c732-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c732-105">DESCRIPTION</span></span>
<span data-ttu-id="3c732-106">Get-AzureRmProviderOperation pobiera operacje udostępnione przez dostawców zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3c732-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="3c732-107">Operacje mogą być składane w celu utworzenia ról niestandardowych w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="3c732-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="3c732-108">Polecenie przyjmuje jako wartość wejściową ciąg wyszukiwania operacji (z możliwymi znakami wieloznacznymi (\*)), który określa szczegóły operacji do wyświetlenia.</span><span class="sxs-lookup"><span data-stu-id="3c732-108">The command takes as input an operation search string (with possible wildcard(\*) character(s)) which determines the operations details to display.</span></span>

<span data-ttu-id="3c732-109">Użyj Get-AzureRmProviderOperation \*, aby pobrać wszystkie operacje dla wszystkich dostawców zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3c732-109">Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers.</span></span>

<span data-ttu-id="3c732-110">Użyj Get-AzureRmProviderOperation Microsoft. COMPUTE/\*, aby pobrać wszystkie operacje dotyczące dostawcy zasobów Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="3c732-110">Use Get-AzureRmProviderOperation Microsoft.Compute/\* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="3c732-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c732-111">EXAMPLES</span></span>

### <span data-ttu-id="3c732-112">Pobierz wszystkie akcje dla wszystkich dostawców</span><span class="sxs-lookup"><span data-stu-id="3c732-112">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="3c732-113">Uzyskiwanie akcji dla określonego dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="3c732-113">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="3c732-114">Uzyskiwanie wszystkich akcji, które można wykonywać na maszynach wirtualnych</span><span class="sxs-lookup"><span data-stu-id="3c732-114">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="3c732-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c732-115">PARAMETERS</span></span>

### <span data-ttu-id="3c732-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c732-116">-DefaultProfile</span></span>
<span data-ttu-id="3c732-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3c732-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c732-118">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="3c732-118">-OperationSearchString</span></span>
<span data-ttu-id="3c732-119">Ciąg wyszukiwania operacji (z możliwymi symbolami wieloznacznymi (\*))</span><span class="sxs-lookup"><span data-stu-id="3c732-119">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c732-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c732-120">CommonParameters</span></span>
<span data-ttu-id="3c732-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c732-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c732-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c732-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c732-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c732-123">INPUTS</span></span>

### <span data-ttu-id="3c732-124">Ciąg</span><span class="sxs-lookup"><span data-stu-id="3c732-124">String</span></span>
<span data-ttu-id="3c732-125">Parametr "OperationSearchString" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="3c732-125">Parameter 'OperationSearchString' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3c732-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c732-126">OUTPUTS</span></span>

### <span data-ttu-id="3c732-127">Microsoft. Azure. Commands. resources. models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3c732-127">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="3c732-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c732-128">NOTES</span></span>
<span data-ttu-id="3c732-129">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="3c732-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3c732-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c732-130">RELATED LINKS</span></span>
