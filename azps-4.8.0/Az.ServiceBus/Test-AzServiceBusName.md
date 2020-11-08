---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: a52274d44b36f2e0dea220464ba835635ab845f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062061"
---
# <span data-ttu-id="0126e-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="0126e-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="0126e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0126e-102">SYNOPSIS</span></span>
<span data-ttu-id="0126e-103">Sprawdza dostępność danej nazwy obszaru nazw lub aliasu (nazwy konfiguracji DR).</span><span class="sxs-lookup"><span data-stu-id="0126e-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="0126e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0126e-104">SYNTAX</span></span>

### <span data-ttu-id="0126e-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0126e-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0126e-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0126e-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0126e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0126e-107">DESCRIPTION</span></span>
<span data-ttu-id="0126e-108">Polecenie cmdlet **test-AzServiceBusName** sprawdza dostępność nazwy obszaru nazw lub aliasu (nazwy konfiguracji dr).</span><span class="sxs-lookup"><span data-stu-id="0126e-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="0126e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0126e-109">EXAMPLES</span></span>

### <span data-ttu-id="0126e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0126e-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="0126e-111">Zwraca stan dostępności nazwy obszaru nazw "MyNameSapceName" jako prawda.</span><span class="sxs-lookup"><span data-stu-id="0126e-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="0126e-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0126e-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="0126e-113">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako FAŁSZ z powodu</span><span class="sxs-lookup"><span data-stu-id="0126e-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="0126e-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0126e-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="0126e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0126e-115">PARAMETERS</span></span>

### <span data-ttu-id="0126e-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="0126e-116">-AliasName</span></span>
<span data-ttu-id="0126e-117">Nazwa konfiguracji DR — Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="0126e-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0126e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0126e-118">-DefaultProfile</span></span>
<span data-ttu-id="0126e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0126e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0126e-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0126e-120">-Namespace</span></span>
<span data-ttu-id="0126e-121">Nazwa przestrzeni nazw ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0126e-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0126e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0126e-122">-ResourceGroupName</span></span>
<span data-ttu-id="0126e-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0126e-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0126e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0126e-124">CommonParameters</span></span>
<span data-ttu-id="0126e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0126e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0126e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0126e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0126e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0126e-127">INPUTS</span></span>

### <span data-ttu-id="0126e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0126e-128">System.String</span></span>

## <span data-ttu-id="0126e-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0126e-129">OUTPUTS</span></span>

### <span data-ttu-id="0126e-130">Microsoft. Azure. Commands. ServiceBus. models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="0126e-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="0126e-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0126e-131">NOTES</span></span>

## <span data-ttu-id="0126e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0126e-132">RELATED LINKS</span></span>
