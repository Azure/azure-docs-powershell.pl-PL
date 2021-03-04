---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: 6c0843afa3001299a21f49cec5ed73f74bdcd2a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955818"
---
# <span data-ttu-id="a5d42-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="a5d42-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="a5d42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d42-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d42-103">Tworzy nową lub aktualizuje istniejącą grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="a5d42-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="a5d42-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a5d42-104">SYNTAX</span></span>

### <span data-ttu-id="a5d42-105">ByPropertyName (Default)</span><span class="sxs-lookup"><span data-stu-id="a5d42-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d42-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5d42-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d42-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5d42-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5d42-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a5d42-108">DESCRIPTION</span></span>
<span data-ttu-id="a5d42-109">Polecenie **cmdlet Set-AzActionGroup** tworzy nową lub aktualizuje istniejącą grupę akcji</span><span class="sxs-lookup"><span data-stu-id="a5d42-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="a5d42-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a5d42-110">EXAMPLES</span></span>

### <span data-ttu-id="a5d42-111">Przykład 1. Tworzenie grupy akcji</span><span class="sxs-lookup"><span data-stu-id="a5d42-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="a5d42-112">Pierwsze dwa polecenia tworzą dwóch odbiorców.</span><span class="sxs-lookup"><span data-stu-id="a5d42-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="a5d42-113">Ostatnie polecenie tworzy grupę akcji z dwoma odbiorcami.</span><span class="sxs-lookup"><span data-stu-id="a5d42-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="a5d42-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5d42-114">PARAMETERS</span></span>

### <span data-ttu-id="a5d42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d42-115">-DefaultProfile</span></span>
<span data-ttu-id="a5d42-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a5d42-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5d42-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="a5d42-117">-DisableGroup</span></span>
<span data-ttu-id="a5d42-118">Wyłącza grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="a5d42-118">Disables the action group.</span></span>

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

### <span data-ttu-id="a5d42-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5d42-119">-InputObject</span></span>
<span data-ttu-id="a5d42-120">Zasób grupy akcji</span><span class="sxs-lookup"><span data-stu-id="a5d42-120">The action group resource</span></span>

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

### <span data-ttu-id="a5d42-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a5d42-121">-Name</span></span>
<span data-ttu-id="a5d42-122">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="a5d42-122">The name of the action group.</span></span>

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

### <span data-ttu-id="a5d42-123">- Odbiorca</span><span class="sxs-lookup"><span data-stu-id="a5d42-123">-Receiver</span></span>
<span data-ttu-id="a5d42-124">Lista odbiorców grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="a5d42-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="a5d42-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d42-125">-ResourceGroupName</span></span>
<span data-ttu-id="a5d42-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a5d42-126">The resource group nam</span></span>

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

### <span data-ttu-id="a5d42-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5d42-127">-ResourceId</span></span>
<span data-ttu-id="a5d42-128">Zasób i</span><span class="sxs-lookup"><span data-stu-id="a5d42-128">The resource i</span></span>

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

### <span data-ttu-id="a5d42-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="a5d42-129">-ShortName</span></span>
<span data-ttu-id="a5d42-130">Krótka nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="a5d42-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="a5d42-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="a5d42-131">-Tag</span></span>
<span data-ttu-id="a5d42-132">Tagi zasobu grupy akcji</span><span class="sxs-lookup"><span data-stu-id="a5d42-132">The tags of the action group resource</span></span>

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

### <span data-ttu-id="a5d42-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5d42-133">-Confirm</span></span>
<span data-ttu-id="a5d42-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a5d42-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d42-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d42-135">-WhatIf</span></span>
<span data-ttu-id="a5d42-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5d42-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5d42-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a5d42-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d42-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d42-138">CommonParameters</span></span>
<span data-ttu-id="a5d42-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d42-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d42-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5d42-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d42-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5d42-141">INPUTS</span></span>

### <span data-ttu-id="a5d42-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a5d42-142">System.String</span></span>

### <span data-ttu-id="a5d42-143">System.Collections.generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlet.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="a5d42-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a5d42-144">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="a5d42-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a5d42-145">System.Collections.Generic.IDictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a5d42-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a5d42-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="a5d42-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="a5d42-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5d42-147">OUTPUTS</span></span>

### <span data-ttu-id="a5d42-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="a5d42-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="a5d42-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a5d42-149">NOTES</span></span>

## <span data-ttu-id="a5d42-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5d42-150">RELATED LINKS</span></span>

<span data-ttu-id="a5d42-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="a5d42-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
