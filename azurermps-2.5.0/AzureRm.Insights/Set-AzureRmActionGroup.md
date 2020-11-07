---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 3f8b3ad20e9a80344227a28dd7cd1f2763cbaab4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897642"
---
# <span data-ttu-id="83330-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="83330-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="83330-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83330-102">SYNOPSIS</span></span>
<span data-ttu-id="83330-103">Umożliwia utworzenie nowej lub zaktualizowanie istniejącej grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="83330-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83330-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83330-104">SYNTAX</span></span>

### <span data-ttu-id="83330-105">ByPropertyName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="83330-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83330-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="83330-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83330-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="83330-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83330-108">Opis</span><span class="sxs-lookup"><span data-stu-id="83330-108">DESCRIPTION</span></span>
<span data-ttu-id="83330-109">Polecenie cmdlet **Set-AzureRmActionGroup** powoduje utworzenie nowej lub zaktualizowanie istniejącej grupy akcji</span><span class="sxs-lookup"><span data-stu-id="83330-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="83330-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83330-110">EXAMPLES</span></span>

### <span data-ttu-id="83330-111">Przykład 1. Tworzenie grupy akcji</span><span class="sxs-lookup"><span data-stu-id="83330-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="83330-112">Dwa pierwsze polecenia tworzą dwa odbiorniki.</span><span class="sxs-lookup"><span data-stu-id="83330-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="83330-113">W ostatnim poleceniu zostanie utworzona grupa akcji zawierająca dwóch odbiorców.</span><span class="sxs-lookup"><span data-stu-id="83330-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="83330-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83330-114">PARAMETERS</span></span>

### <span data-ttu-id="83330-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83330-115">-DefaultProfile</span></span>
<span data-ttu-id="83330-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="83330-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83330-117">-Disable</span><span class="sxs-lookup"><span data-stu-id="83330-117">-DisableGroup</span></span>
<span data-ttu-id="83330-118">Wyłącza grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="83330-118">Disables the action group.</span></span>

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

### <span data-ttu-id="83330-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="83330-119">-InputObject</span></span>
<span data-ttu-id="83330-120">Grupa akcji resourc</span><span class="sxs-lookup"><span data-stu-id="83330-120">The action group resourc</span></span>

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

### <span data-ttu-id="83330-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="83330-121">-Name</span></span>
<span data-ttu-id="83330-122">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="83330-122">The name of the action group.</span></span>

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

### <span data-ttu-id="83330-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="83330-123">-Receiver</span></span>
<span data-ttu-id="83330-124">Lista odbiorców grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="83330-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="83330-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83330-125">-ResourceGroupName</span></span>
<span data-ttu-id="83330-126">Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="83330-126">The resource group nam</span></span>

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

### <span data-ttu-id="83330-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83330-127">-ResourceId</span></span>
<span data-ttu-id="83330-128">Zasób i</span><span class="sxs-lookup"><span data-stu-id="83330-128">The resource i</span></span>

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

### <span data-ttu-id="83330-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="83330-129">-ShortName</span></span>
<span data-ttu-id="83330-130">Krótka nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="83330-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="83330-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="83330-131">-Tag</span></span>
<span data-ttu-id="83330-132">Tagi resourc grupy akcji</span><span class="sxs-lookup"><span data-stu-id="83330-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="83330-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83330-133">-Confirm</span></span>
<span data-ttu-id="83330-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83330-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83330-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83330-135">-WhatIf</span></span>
<span data-ttu-id="83330-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83330-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83330-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83330-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83330-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83330-138">CommonParameters</span></span>
<span data-ttu-id="83330-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83330-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83330-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83330-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83330-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83330-141">INPUTS</span></span>

### <span data-ttu-id="83330-142">System. String</span><span class="sxs-lookup"><span data-stu-id="83330-142">System.String</span></span>

### <span data-ttu-id="83330-143">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Insights.. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="83330-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="83330-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="83330-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="83330-145">System. Collections. Generic. IDictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="83330-145">System.Collections.Generic.IDictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="83330-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="83330-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="83330-147">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="83330-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="83330-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83330-148">OUTPUTS</span></span>

### <span data-ttu-id="83330-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="83330-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="83330-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83330-150">NOTES</span></span>

## <span data-ttu-id="83330-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83330-151">RELATED LINKS</span></span>

<span data-ttu-id="83330-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Nowe — AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="83330-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
