---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: bae9d8814d5988d0d509f64cb1de10040bb1af00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554087"
---
# <span data-ttu-id="b3a9f-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="b3a9f-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="b3a9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a9f-103">Umożliwia utworzenie nowej lub zaktualizowanie istniejącej grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3a9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3a9f-104">SYNTAX</span></span>

### <span data-ttu-id="b3a9f-105">ByPropertyName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3a9f-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a9f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a9f-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a9f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3a9f-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3a9f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b3a9f-108">DESCRIPTION</span></span>
<span data-ttu-id="b3a9f-109">Polecenie cmdlet **Set-AzureRmActionGroup** powoduje utworzenie nowej lub zaktualizowanie istniejącej grupy akcji</span><span class="sxs-lookup"><span data-stu-id="b3a9f-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="b3a9f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3a9f-110">EXAMPLES</span></span>

### <span data-ttu-id="b3a9f-111">Przykład 1. Tworzenie grupy akcji</span><span class="sxs-lookup"><span data-stu-id="b3a9f-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="b3a9f-112">Dwa pierwsze polecenia tworzą dwa odbiorniki.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="b3a9f-113">W ostatnim poleceniu zostanie utworzona grupa akcji zawierająca dwóch odbiorców.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="b3a9f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3a9f-114">PARAMETERS</span></span>

### <span data-ttu-id="b3a9f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a9f-115">-DefaultProfile</span></span>
<span data-ttu-id="b3a9f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b3a9f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3a9f-117">-Disable</span><span class="sxs-lookup"><span data-stu-id="b3a9f-117">-DisableGroup</span></span>
<span data-ttu-id="b3a9f-118">Wyłącza grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-118">Disables the action group.</span></span>

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

### <span data-ttu-id="b3a9f-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3a9f-119">-InputObject</span></span>
<span data-ttu-id="b3a9f-120">Grupa akcji resourc</span><span class="sxs-lookup"><span data-stu-id="b3a9f-120">The action group resourc</span></span>

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

### <span data-ttu-id="b3a9f-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3a9f-121">-Name</span></span>
<span data-ttu-id="b3a9f-122">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-122">The name of the action group.</span></span>

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

### <span data-ttu-id="b3a9f-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="b3a9f-123">-Receiver</span></span>
<span data-ttu-id="b3a9f-124">Lista odbiorców grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="b3a9f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a9f-125">-ResourceGroupName</span></span>
<span data-ttu-id="b3a9f-126">Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="b3a9f-126">The resource group nam</span></span>

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

### <span data-ttu-id="b3a9f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a9f-127">-ResourceId</span></span>
<span data-ttu-id="b3a9f-128">Zasób i</span><span class="sxs-lookup"><span data-stu-id="b3a9f-128">The resource i</span></span>

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

### <span data-ttu-id="b3a9f-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="b3a9f-129">-ShortName</span></span>
<span data-ttu-id="b3a9f-130">Krótka nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="b3a9f-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3a9f-131">-Tag</span></span>
<span data-ttu-id="b3a9f-132">Tagi resourc grupy akcji</span><span class="sxs-lookup"><span data-stu-id="b3a9f-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="b3a9f-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3a9f-133">-Confirm</span></span>
<span data-ttu-id="b3a9f-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3a9f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a9f-135">-WhatIf</span></span>
<span data-ttu-id="b3a9f-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3a9f-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3a9f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a9f-138">CommonParameters</span></span>
<span data-ttu-id="b3a9f-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a9f-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3a9f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a9f-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3a9f-141">INPUTS</span></span>

### <span data-ttu-id="b3a9f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b3a9f-142">System.String</span></span>

### <span data-ttu-id="b3a9f-143">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Insights.. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b3a9f-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b3a9f-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3a9f-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b3a9f-145">System. Collections. Generic. IDictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b3a9f-145">System.Collections.Generic.IDictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b3a9f-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="b3a9f-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="b3a9f-147">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b3a9f-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b3a9f-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3a9f-148">OUTPUTS</span></span>

### <span data-ttu-id="b3a9f-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="b3a9f-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="b3a9f-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3a9f-150">NOTES</span></span>

## <span data-ttu-id="b3a9f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3a9f-151">RELATED LINKS</span></span>

<span data-ttu-id="b3a9f-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Nowe — AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="b3a9f-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
