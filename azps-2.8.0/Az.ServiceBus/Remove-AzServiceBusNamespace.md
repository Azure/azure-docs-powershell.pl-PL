---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: b17fa7309274f261c329eaf896519f8bb70d06fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873124"
---
# <span data-ttu-id="c1929-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="c1929-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="c1929-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1929-102">SYNOPSIS</span></span>
<span data-ttu-id="c1929-103">Usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1929-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="c1929-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1929-104">SYNTAX</span></span>

### <span data-ttu-id="c1929-105">NamespacePropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c1929-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1929-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c1929-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1929-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1929-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1929-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c1929-108">DESCRIPTION</span></span>
<span data-ttu-id="c1929-109">Polecenie cmdlet **Remove-AzServiceBusNamespace** usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1929-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="c1929-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1929-110">EXAMPLES</span></span>

### <span data-ttu-id="c1929-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1929-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="c1929-112">Usuwa obszar nazw usługi Service Bus `SB-Example1` z określonej grupy zasobów `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="c1929-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="c1929-113">Przykład 2,1-wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="c1929-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="c1929-114">Usuwa obszar nazw usługi Service Bus udostępniony za pośrednictwem $inputobject.</span><span class="sxs-lookup"><span data-stu-id="c1929-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="c1929-115">Przykład 2,2-Inputobject-przy użyciu instalacji rurowej:</span><span class="sxs-lookup"><span data-stu-id="c1929-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="c1929-116">Usuwa obszar nazw usługi Service Bus za pomocą połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="c1929-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="c1929-117">Przykład 3-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1929-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="c1929-118">Usuwa obszar nazw usługi Service Bus podany za pośrednictwem identyfikatora ARM w $resourceid parametru-ResourceId lub za pośrednictwem połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="c1929-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="c1929-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1929-119">PARAMETERS</span></span>

### <span data-ttu-id="c1929-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1929-120">-AsJob</span></span>
<span data-ttu-id="c1929-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c1929-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1929-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1929-122">-DefaultProfile</span></span>
<span data-ttu-id="c1929-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1929-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1929-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c1929-124">-InputObject</span></span>
<span data-ttu-id="c1929-125">Obiekt obszaru nazw magistrali usług</span><span class="sxs-lookup"><span data-stu-id="c1929-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1929-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c1929-126">-Name</span></span>
<span data-ttu-id="c1929-127">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="c1929-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1929-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1929-128">-PassThru</span></span>
<span data-ttu-id="c1929-129">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="c1929-129">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1929-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1929-130">-ResourceGroupName</span></span>
<span data-ttu-id="c1929-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c1929-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1929-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1929-132">-ResourceId</span></span>
<span data-ttu-id="c1929-133">Identyfikator zasobu obszaru nazw usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="c1929-133">Service Bus Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1929-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1929-134">-Confirm</span></span>
<span data-ttu-id="c1929-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1929-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1929-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1929-136">-WhatIf</span></span>
<span data-ttu-id="c1929-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1929-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1929-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c1929-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1929-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1929-139">CommonParameters</span></span>
<span data-ttu-id="c1929-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1929-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1929-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1929-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1929-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1929-142">INPUTS</span></span>

### <span data-ttu-id="c1929-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c1929-143">System.String</span></span>

### <span data-ttu-id="c1929-144">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c1929-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c1929-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1929-145">OUTPUTS</span></span>

### <span data-ttu-id="c1929-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1929-146">System.Boolean</span></span>

## <span data-ttu-id="c1929-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1929-147">NOTES</span></span>

## <span data-ttu-id="c1929-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1929-148">RELATED LINKS</span></span>
