---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: b2bca900be878e6f89f52b1f6096e82f79ec7863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961585"
---
# <span data-ttu-id="a0602-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="a0602-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="a0602-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0602-102">SYNOPSIS</span></span>
<span data-ttu-id="a0602-103">Sprawdza dostępność danej nazwy lub aliasu NameSpace (nazwa konfiguracji DR).</span><span class="sxs-lookup"><span data-stu-id="a0602-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="a0602-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0602-104">SYNTAX</span></span>

### <span data-ttu-id="a0602-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a0602-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0602-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a0602-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0602-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0602-107">DESCRIPTION</span></span>
<span data-ttu-id="a0602-108">Polecenie **cmdlet Test-AzServiceBusName** sprawdza dostępność nazwy lub aliasu NameSpace (nazwa konfiguracji DR)</span><span class="sxs-lookup"><span data-stu-id="a0602-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="a0602-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0602-109">EXAMPLES</span></span>

### <span data-ttu-id="a0602-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0602-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="a0602-111">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako prawda.</span><span class="sxs-lookup"><span data-stu-id="a0602-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="a0602-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a0602-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="a0602-113">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako Fałsz z powodu.</span><span class="sxs-lookup"><span data-stu-id="a0602-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="a0602-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a0602-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="a0602-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0602-115">PARAMETERS</span></span>

### <span data-ttu-id="a0602-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="a0602-116">-AliasName</span></span>
<span data-ttu-id="a0602-117">Nazwa konfiguracji dr — nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="a0602-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="a0602-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0602-118">-DefaultProfile</span></span>
<span data-ttu-id="a0602-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0602-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0602-120">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="a0602-120">-Namespace</span></span>
<span data-ttu-id="a0602-121">Nazwa przestrzeni nazw usługi Servicebus</span><span class="sxs-lookup"><span data-stu-id="a0602-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="a0602-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0602-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0602-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a0602-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a0602-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0602-124">CommonParameters</span></span>
<span data-ttu-id="a0602-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0602-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0602-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0602-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0602-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0602-127">INPUTS</span></span>

### <span data-ttu-id="a0602-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a0602-128">System.String</span></span>

## <span data-ttu-id="a0602-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0602-129">OUTPUTS</span></span>

### <span data-ttu-id="a0602-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="a0602-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="a0602-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0602-131">NOTES</span></span>

## <span data-ttu-id="a0602-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0602-132">RELATED LINKS</span></span>
