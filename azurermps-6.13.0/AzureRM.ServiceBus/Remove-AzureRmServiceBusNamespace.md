---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: c56637b8470e40e6b46984117a764da248684005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716917"
---
# <span data-ttu-id="bee6f-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="bee6f-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="bee6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bee6f-102">SYNOPSIS</span></span>
<span data-ttu-id="bee6f-103">Usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bee6f-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bee6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bee6f-104">SYNTAX</span></span>

### <span data-ttu-id="bee6f-105">NamespacePropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bee6f-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bee6f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bee6f-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bee6f-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bee6f-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bee6f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bee6f-108">DESCRIPTION</span></span>
<span data-ttu-id="bee6f-109">Polecenie cmdlet **Remove-AzureRmServiceBusNamespace** usuwa obszar nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bee6f-109">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="bee6f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bee6f-110">EXAMPLES</span></span>

### <span data-ttu-id="bee6f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bee6f-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="bee6f-112">Usuwa obszar nazw usługi Service Bus `SB-Example1` z określonej grupy zasobów `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="bee6f-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="bee6f-113">Przykład 2,1-wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="bee6f-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusNamespace <params>
PS C:\> Remove-AzureRmServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="bee6f-114">Usuwa obszar nazw usługi Service Bus udostępniony za pośrednictwem $inputobject.</span><span class="sxs-lookup"><span data-stu-id="bee6f-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="bee6f-115">Przykład 2,2-Inputobject-przy użyciu instalacji rurowej:</span><span class="sxs-lookup"><span data-stu-id="bee6f-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace <params> | Remove-AzureRmServiceBusNamespace
```

<span data-ttu-id="bee6f-116">Usuwa obszar nazw usługi Service Bus za pomocą połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="bee6f-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="bee6f-117">Przykład 3-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bee6f-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzureRmResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="bee6f-118">Usuwa obszar nazw usługi Service Bus podany za pośrednictwem identyfikatora ARM w $resourceid parametru-ResourceId lub za pośrednictwem połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="bee6f-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="bee6f-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bee6f-119">PARAMETERS</span></span>

### <span data-ttu-id="bee6f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bee6f-120">-AsJob</span></span>
<span data-ttu-id="bee6f-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bee6f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bee6f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee6f-122">-DefaultProfile</span></span>
<span data-ttu-id="bee6f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bee6f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee6f-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bee6f-124">-InputObject</span></span>
<span data-ttu-id="bee6f-125">Obiekt obszaru nazw magistrali usług</span><span class="sxs-lookup"><span data-stu-id="bee6f-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="bee6f-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bee6f-126">-Name</span></span>
<span data-ttu-id="bee6f-127">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="bee6f-127">Namespace Name.</span></span>

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

### <span data-ttu-id="bee6f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bee6f-128">-PassThru</span></span>
<span data-ttu-id="bee6f-129">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="bee6f-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="bee6f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee6f-130">-ResourceGroupName</span></span>
<span data-ttu-id="bee6f-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bee6f-131">The name of the resource group</span></span>

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

### <span data-ttu-id="bee6f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bee6f-132">-ResourceId</span></span>
<span data-ttu-id="bee6f-133">Identyfikator zasobu obszaru nazw usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="bee6f-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="bee6f-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bee6f-134">-Confirm</span></span>
<span data-ttu-id="bee6f-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee6f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bee6f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bee6f-136">-WhatIf</span></span>
<span data-ttu-id="bee6f-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee6f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bee6f-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bee6f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bee6f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee6f-139">CommonParameters</span></span>
<span data-ttu-id="bee6f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee6f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee6f-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bee6f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee6f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bee6f-142">INPUTS</span></span>

### <span data-ttu-id="bee6f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bee6f-143">System.String</span></span>

### <span data-ttu-id="bee6f-144">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bee6f-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="bee6f-145">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bee6f-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bee6f-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bee6f-146">OUTPUTS</span></span>

### <span data-ttu-id="bee6f-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bee6f-147">System.Boolean</span></span>

## <span data-ttu-id="bee6f-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bee6f-148">NOTES</span></span>

## <span data-ttu-id="bee6f-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bee6f-149">RELATED LINKS</span></span>
