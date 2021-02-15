---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: ede2a8566f7305b4f56a5fc392090b426c148547
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399009"
---
# <span data-ttu-id="1f5d6-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="1f5d6-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="1f5d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f5d6-102">SYNOPSIS</span></span>
<span data-ttu-id="1f5d6-103">Tworzy nową lub aktualizuje istniejącą grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="1f5d6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1f5d6-104">SYNTAX</span></span>

### <span data-ttu-id="1f5d6-105">ByPropertyName (Default)</span><span class="sxs-lookup"><span data-stu-id="1f5d6-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f5d6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f5d6-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f5d6-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1f5d6-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f5d6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1f5d6-108">DESCRIPTION</span></span>
<span data-ttu-id="1f5d6-109">Polecenie **cmdlet Set-AzActionGroup** tworzy nową lub aktualizuje istniejącą grupę akcji</span><span class="sxs-lookup"><span data-stu-id="1f5d6-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="1f5d6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1f5d6-110">EXAMPLES</span></span>

### <span data-ttu-id="1f5d6-111">Przykład 1. Tworzenie grupy akcji</span><span class="sxs-lookup"><span data-stu-id="1f5d6-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="1f5d6-112">Pierwsze dwa polecenia tworzą dwóch odbiorców.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="1f5d6-113">Ostatnie polecenie tworzy grupę akcji z dwoma odbiorcami.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="1f5d6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f5d6-114">PARAMETERS</span></span>

### <span data-ttu-id="1f5d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f5d6-115">-DefaultProfile</span></span>
<span data-ttu-id="1f5d6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1f5d6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f5d6-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="1f5d6-117">-DisableGroup</span></span>
<span data-ttu-id="1f5d6-118">Wyłącza grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-118">Disables the action group.</span></span>

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

### <span data-ttu-id="1f5d6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f5d6-119">-InputObject</span></span>
<span data-ttu-id="1f5d6-120">Zasób grupy akcji</span><span class="sxs-lookup"><span data-stu-id="1f5d6-120">The action group resource</span></span>

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

### <span data-ttu-id="1f5d6-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1f5d6-121">-Name</span></span>
<span data-ttu-id="1f5d6-122">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-122">The name of the action group.</span></span>

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

### <span data-ttu-id="1f5d6-123">- Odbiorca</span><span class="sxs-lookup"><span data-stu-id="1f5d6-123">-Receiver</span></span>
<span data-ttu-id="1f5d6-124">Lista odbiorców grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="1f5d6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f5d6-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f5d6-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1f5d6-126">The resource group nam</span></span>

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

### <span data-ttu-id="1f5d6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f5d6-127">-ResourceId</span></span>
<span data-ttu-id="1f5d6-128">Zasób i</span><span class="sxs-lookup"><span data-stu-id="1f5d6-128">The resource i</span></span>

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

### <span data-ttu-id="1f5d6-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="1f5d6-129">-ShortName</span></span>
<span data-ttu-id="1f5d6-130">Krótka nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="1f5d6-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="1f5d6-131">-Tag</span></span>
<span data-ttu-id="1f5d6-132">Tagi zasobu grupy akcji</span><span class="sxs-lookup"><span data-stu-id="1f5d6-132">The tags of the action group resource</span></span>

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

### <span data-ttu-id="1f5d6-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f5d6-133">-Confirm</span></span>
<span data-ttu-id="1f5d6-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f5d6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f5d6-135">-WhatIf</span></span>
<span data-ttu-id="1f5d6-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f5d6-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f5d6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f5d6-138">CommonParameters</span></span>
<span data-ttu-id="1f5d6-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f5d6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f5d6-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f5d6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f5d6-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f5d6-141">INPUTS</span></span>

### <span data-ttu-id="1f5d6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1f5d6-142">System.String</span></span>

### <span data-ttu-id="1f5d6-143">System.Collections.generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlet.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="1f5d6-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1f5d6-144">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="1f5d6-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1f5d6-145">System.Collections.Generic.IDictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1f5d6-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1f5d6-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="1f5d6-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="1f5d6-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f5d6-147">OUTPUTS</span></span>

### <span data-ttu-id="1f5d6-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="1f5d6-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="1f5d6-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1f5d6-149">NOTES</span></span>

## <span data-ttu-id="1f5d6-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f5d6-150">RELATED LINKS</span></span>

<span data-ttu-id="1f5d6-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="1f5d6-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>

