---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
ms.openlocfilehash: 9598280ecae0ce8aca94fd16ae40928dba7a2404
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542004"
---
# <span data-ttu-id="bb6a0-101">Remove-AzureRmAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="bb6a0-101">Remove-AzureRmAutomationConnectionType</span></span>

## <span data-ttu-id="bb6a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb6a0-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6a0-103">Usuwa typ połączenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-103">Removes an Automation connection type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb6a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb6a0-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb6a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb6a0-105">DESCRIPTION</span></span>
<span data-ttu-id="bb6a0-106">Polecenie cmdlet **Remove-AzureRmAutomationConnectionType** usuwa typ połączenia z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-106">The **Remove-AzureRmAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="bb6a0-107">Wszystkie połączenia skojarzone z usuniętym typem połączenia staną się nieużyteczne.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="bb6a0-108">Można je usunąć, chyba że zostanie utworzony nowy typ połączenia spełniający następujące kryteria:</span><span class="sxs-lookup"><span data-stu-id="bb6a0-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="bb6a0-109">Typ ma taką samą nazwę jak oryginalny typ połączenia.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="bb6a0-110">Typ ma te same definicje pól co oryginalny typ połączenia.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="bb6a0-111">Może zawierać dodatkowe pola.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-111">It can have additional fields.</span></span>

## <span data-ttu-id="bb6a0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb6a0-112">EXAMPLES</span></span>

### <span data-ttu-id="bb6a0-113">Przykład 1. Usuń typ połączenia</span><span class="sxs-lookup"><span data-stu-id="bb6a0-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzureRmAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bb6a0-114">To polecenie usuwa typ połączenia o nazwie ContosoConnectionType na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="bb6a0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb6a0-115">PARAMETERS</span></span>

### <span data-ttu-id="bb6a0-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bb6a0-116">-AutomationAccountName</span></span>
<span data-ttu-id="bb6a0-117">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa typ połączenia.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="bb6a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6a0-118">-DefaultProfile</span></span>
<span data-ttu-id="bb6a0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bb6a0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb6a0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bb6a0-120">-Force</span></span>
<span data-ttu-id="bb6a0-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="bb6a0-121">ps_force</span></span>

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

### <span data-ttu-id="bb6a0-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb6a0-122">-Name</span></span>
<span data-ttu-id="bb6a0-123">Określa nazwę typu połączenia automatyzacji, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bb6a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb6a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb6a0-125">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa typ połączenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="bb6a0-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb6a0-126">-Confirm</span></span>
<span data-ttu-id="bb6a0-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb6a0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb6a0-128">-WhatIf</span></span>
<span data-ttu-id="bb6a0-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb6a0-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb6a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6a0-131">CommonParameters</span></span>
<span data-ttu-id="bb6a0-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb6a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6a0-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb6a0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6a0-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb6a0-134">INPUTS</span></span>

### <span data-ttu-id="bb6a0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bb6a0-135">System.String</span></span>

## <span data-ttu-id="bb6a0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb6a0-136">OUTPUTS</span></span>

### <span data-ttu-id="bb6a0-137">System. void</span><span class="sxs-lookup"><span data-stu-id="bb6a0-137">System.Void</span></span>

## <span data-ttu-id="bb6a0-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb6a0-138">NOTES</span></span>

## <span data-ttu-id="bb6a0-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb6a0-139">RELATED LINKS</span></span>

[<span data-ttu-id="bb6a0-140">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="bb6a0-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


