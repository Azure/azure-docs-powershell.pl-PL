---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 4d153a05ad245eeece671adced6aa2f8029dc9a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009962"
---
# <span data-ttu-id="3e1bc-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="3e1bc-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="3e1bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1bc-103">Usuwa typ połączenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="3e1bc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3e1bc-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e1bc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3e1bc-105">DESCRIPTION</span></span>
<span data-ttu-id="3e1bc-106">Polecenie **cmdlet Remove-AzAutomationConnectionType** usuwa typ połączenia z automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="3e1bc-107">Wszystkie połączenia skojarzone z usuniętym typem połączenia stają się bezużytelne.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="3e1bc-108">Usuń je, chyba że utworzysz nowy typ połączenia spełniający następujące kryteria:</span><span class="sxs-lookup"><span data-stu-id="3e1bc-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="3e1bc-109">Typ ma taką samą nazwę jak oryginalny typ połączenia.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="3e1bc-110">Typ ma te same definicje pól, co oryginalny typ połączenia.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="3e1bc-111">Może ona mieć dodatkowe pola.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-111">It can have additional fields.</span></span>

## <span data-ttu-id="3e1bc-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3e1bc-112">EXAMPLES</span></span>

### <span data-ttu-id="3e1bc-113">Przykład 1. Usuwanie typu połączenia</span><span class="sxs-lookup"><span data-stu-id="3e1bc-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3e1bc-114">To polecenie usuwa typ połączenia o nazwie ContosoConnectionType z konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3e1bc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e1bc-115">PARAMETERS</span></span>

### <span data-ttu-id="3e1bc-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3e1bc-116">-AutomationAccountName</span></span>
<span data-ttu-id="3e1bc-117">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa typ połączenia.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1bc-118">-DefaultProfile</span></span>
<span data-ttu-id="3e1bc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3e1bc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e1bc-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3e1bc-120">-Force</span></span>
<span data-ttu-id="3e1bc-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="3e1bc-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1bc-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3e1bc-122">-Name</span></span>
<span data-ttu-id="3e1bc-123">Określa nazwę typu połączenia automatyzacji, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1bc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1bc-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e1bc-125">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa typ połączenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1bc-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e1bc-126">-Confirm</span></span>
<span data-ttu-id="3e1bc-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1bc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e1bc-128">-WhatIf</span></span>
<span data-ttu-id="3e1bc-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e1bc-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1bc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1bc-131">CommonParameters</span></span>
<span data-ttu-id="3e1bc-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e1bc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1bc-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e1bc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1bc-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e1bc-134">INPUTS</span></span>

### <span data-ttu-id="3e1bc-135">System.String</span><span class="sxs-lookup"><span data-stu-id="3e1bc-135">System.String</span></span>

## <span data-ttu-id="3e1bc-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e1bc-136">OUTPUTS</span></span>

### <span data-ttu-id="3e1bc-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="3e1bc-137">System.Void</span></span>

## <span data-ttu-id="3e1bc-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3e1bc-138">NOTES</span></span>

## <span data-ttu-id="3e1bc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e1bc-139">RELATED LINKS</span></span>

[<span data-ttu-id="3e1bc-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3e1bc-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


