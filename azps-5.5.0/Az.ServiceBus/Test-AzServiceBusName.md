---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: a52274d44b36f2e0dea220464ba835635ab845f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178579"
---
# <span data-ttu-id="36af6-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="36af6-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="36af6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36af6-102">SYNOPSIS</span></span>
<span data-ttu-id="36af6-103">Sprawdza dostępność podanej nazwy lub aliasu NameSpace (nazwa konfiguracji DR)</span><span class="sxs-lookup"><span data-stu-id="36af6-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="36af6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36af6-104">SYNTAX</span></span>

### <span data-ttu-id="36af6-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="36af6-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36af6-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="36af6-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36af6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="36af6-107">DESCRIPTION</span></span>
<span data-ttu-id="36af6-108">Polecenie **cmdlet Test-AzServiceBusName** sprawdza dostępność nazwy lub aliasu NameSpace (nazwa konfiguracji DR)</span><span class="sxs-lookup"><span data-stu-id="36af6-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="36af6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36af6-109">EXAMPLES</span></span>

### <span data-ttu-id="36af6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36af6-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="36af6-111">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako prawda.</span><span class="sxs-lookup"><span data-stu-id="36af6-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="36af6-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="36af6-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="36af6-113">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako Fałsz z powodu.</span><span class="sxs-lookup"><span data-stu-id="36af6-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="36af6-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="36af6-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="36af6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36af6-115">PARAMETERS</span></span>

### <span data-ttu-id="36af6-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="36af6-116">-AliasName</span></span>
<span data-ttu-id="36af6-117">Nazwa konfiguracji dr — nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="36af6-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="36af6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36af6-118">-DefaultProfile</span></span>
<span data-ttu-id="36af6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="36af6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36af6-120">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="36af6-120">-Namespace</span></span>
<span data-ttu-id="36af6-121">Nazwa przestrzeni nazw usługi Servicebus</span><span class="sxs-lookup"><span data-stu-id="36af6-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="36af6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36af6-122">-ResourceGroupName</span></span>
<span data-ttu-id="36af6-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="36af6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="36af6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36af6-124">CommonParameters</span></span>
<span data-ttu-id="36af6-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36af6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36af6-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36af6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36af6-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36af6-127">INPUTS</span></span>

### <span data-ttu-id="36af6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="36af6-128">System.String</span></span>

## <span data-ttu-id="36af6-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36af6-129">OUTPUTS</span></span>

### <span data-ttu-id="36af6-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="36af6-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="36af6-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36af6-131">NOTES</span></span>

## <span data-ttu-id="36af6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36af6-132">RELATED LINKS</span></span>
