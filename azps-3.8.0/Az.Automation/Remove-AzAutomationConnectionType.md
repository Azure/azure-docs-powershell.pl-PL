---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053903"
---
# <span data-ttu-id="dfd2b-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="dfd2b-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="dfd2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dfd2b-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd2b-103">Usuwa typ połączenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="dfd2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dfd2b-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfd2b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dfd2b-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd2b-106">Polecenie cmdlet **Remove-AzAutomationConnectionType** usuwa typ połączenia z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="dfd2b-107">Wszystkie połączenia skojarzone z usuniętym typem połączenia staną się nieużyteczne.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="dfd2b-108">Można je usunąć, chyba że zostanie utworzony nowy typ połączenia spełniający następujące kryteria:</span><span class="sxs-lookup"><span data-stu-id="dfd2b-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="dfd2b-109">Typ ma taką samą nazwę jak oryginalny typ połączenia.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="dfd2b-110">Typ ma te same definicje pól co oryginalny typ połączenia.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="dfd2b-111">Może zawierać dodatkowe pola.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-111">It can have additional fields.</span></span>

## <span data-ttu-id="dfd2b-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dfd2b-112">EXAMPLES</span></span>

### <span data-ttu-id="dfd2b-113">Przykład 1. Usuń typ połączenia</span><span class="sxs-lookup"><span data-stu-id="dfd2b-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dfd2b-114">To polecenie usuwa typ połączenia o nazwie ContosoConnectionType na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="dfd2b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dfd2b-115">PARAMETERS</span></span>

### <span data-ttu-id="dfd2b-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dfd2b-116">-AutomationAccountName</span></span>
<span data-ttu-id="dfd2b-117">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa typ połączenia.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="dfd2b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd2b-118">-DefaultProfile</span></span>
<span data-ttu-id="dfd2b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dfd2b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfd2b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dfd2b-120">-Force</span></span>
<span data-ttu-id="dfd2b-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="dfd2b-121">ps_force</span></span>

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

### <span data-ttu-id="dfd2b-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dfd2b-122">-Name</span></span>
<span data-ttu-id="dfd2b-123">Określa nazwę typu połączenia automatyzacji, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dfd2b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfd2b-124">-ResourceGroupName</span></span>
<span data-ttu-id="dfd2b-125">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa typ połączenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="dfd2b-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dfd2b-126">-Confirm</span></span>
<span data-ttu-id="dfd2b-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfd2b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd2b-128">-WhatIf</span></span>
<span data-ttu-id="dfd2b-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfd2b-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfd2b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd2b-131">CommonParameters</span></span>
<span data-ttu-id="dfd2b-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd2b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd2b-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd2b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd2b-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfd2b-134">INPUTS</span></span>

### <span data-ttu-id="dfd2b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dfd2b-135">System.String</span></span>

## <span data-ttu-id="dfd2b-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dfd2b-136">OUTPUTS</span></span>

### <span data-ttu-id="dfd2b-137">System. void</span><span class="sxs-lookup"><span data-stu-id="dfd2b-137">System.Void</span></span>

## <span data-ttu-id="dfd2b-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dfd2b-138">NOTES</span></span>

## <span data-ttu-id="dfd2b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfd2b-139">RELATED LINKS</span></span>

[<span data-ttu-id="dfd2b-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="dfd2b-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


