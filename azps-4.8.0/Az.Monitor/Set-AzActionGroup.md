---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: b10aad8cdf480dd567b0646fb3befa95fb32bf72
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220589"
---
# <span data-ttu-id="1f733-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="1f733-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="1f733-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f733-102">SYNOPSIS</span></span>
<span data-ttu-id="1f733-103">Umożliwia utworzenie nowej lub zaktualizowanie istniejącej grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="1f733-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="1f733-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f733-104">SYNTAX</span></span>

### <span data-ttu-id="1f733-105">ByPropertyName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1f733-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f733-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f733-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f733-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1f733-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f733-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1f733-108">DESCRIPTION</span></span>
<span data-ttu-id="1f733-109">Polecenie cmdlet **Set-AzActionGroup** powoduje utworzenie nowej lub zaktualizowanie istniejącej grupy akcji</span><span class="sxs-lookup"><span data-stu-id="1f733-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="1f733-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f733-110">EXAMPLES</span></span>

### <span data-ttu-id="1f733-111">Przykład 1. Tworzenie grupy akcji</span><span class="sxs-lookup"><span data-stu-id="1f733-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="1f733-112">Dwa pierwsze polecenia tworzą dwa odbiorniki.</span><span class="sxs-lookup"><span data-stu-id="1f733-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="1f733-113">W ostatnim poleceniu zostanie utworzona grupa akcji zawierająca dwóch odbiorców.</span><span class="sxs-lookup"><span data-stu-id="1f733-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="1f733-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f733-114">PARAMETERS</span></span>

### <span data-ttu-id="1f733-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f733-115">-DefaultProfile</span></span>
<span data-ttu-id="1f733-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1f733-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f733-117">-Disable</span><span class="sxs-lookup"><span data-stu-id="1f733-117">-DisableGroup</span></span>
<span data-ttu-id="1f733-118">Wyłącza grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="1f733-118">Disables the action group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f733-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1f733-119">-InputObject</span></span>
<span data-ttu-id="1f733-120">Zasób grupa akcji</span><span class="sxs-lookup"><span data-stu-id="1f733-120">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f733-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f733-121">-Name</span></span>
<span data-ttu-id="1f733-122">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="1f733-122">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f733-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="1f733-123">-Receiver</span></span>
<span data-ttu-id="1f733-124">Lista odbiorców grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="1f733-124">The list of receivers of the action group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f733-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f733-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f733-126">Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="1f733-126">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f733-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f733-127">-ResourceId</span></span>
<span data-ttu-id="1f733-128">Zasób i</span><span class="sxs-lookup"><span data-stu-id="1f733-128">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f733-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="1f733-129">-ShortName</span></span>
<span data-ttu-id="1f733-130">Krótka nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="1f733-130">The short name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f733-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f733-131">-Tag</span></span>
<span data-ttu-id="1f733-132">Znaczniki zasobu grupa akcji</span><span class="sxs-lookup"><span data-stu-id="1f733-132">The tags of the action group resource</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f733-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f733-133">-Confirm</span></span>
<span data-ttu-id="1f733-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f733-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f733-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f733-135">-WhatIf</span></span>
<span data-ttu-id="1f733-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f733-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f733-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f733-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f733-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f733-138">CommonParameters</span></span>
<span data-ttu-id="1f733-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f733-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f733-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f733-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f733-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f733-141">INPUTS</span></span>

### <span data-ttu-id="1f733-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1f733-142">System.String</span></span>

### <span data-ttu-id="1f733-143">System. Collections. Generic. list "1 [[Microsoft. Azure. polecenia....... w. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. PowerShell. cmdlets. Monitor, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1f733-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1f733-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1f733-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1f733-145">System. Collections. Generic. IDictionary ' 2 [[System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = 7cec85d7bea7798e], [System. String, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1f733-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1f733-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="1f733-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="1f733-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f733-147">OUTPUTS</span></span>

### <span data-ttu-id="1f733-148">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="1f733-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="1f733-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f733-149">NOTES</span></span>

## <span data-ttu-id="1f733-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f733-150">RELATED LINKS</span></span>

<span data-ttu-id="1f733-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [Nowe — AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="1f733-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
