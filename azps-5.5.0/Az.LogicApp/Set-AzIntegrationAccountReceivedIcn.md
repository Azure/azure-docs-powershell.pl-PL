---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 146f1ba93a8df5f6a4396c30c9da451cdb89b9b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187554"
---
# <span data-ttu-id="bdec3-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="bdec3-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="bdec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdec3-102">SYNOPSIS</span></span>
<span data-ttu-id="bdec3-103">Aktualizuje numer kontroli wymiany (ICN) na koncie integracji w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bdec3-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="bdec3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bdec3-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdec3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bdec3-105">DESCRIPTION</span></span>
<span data-ttu-id="bdec3-106">Polecenie Set-AzIntegrationAccountGeneratedIcn cmdlet aktualizuje istniejący numer kontrolki wymiany odebranego konta integracji (ICN) i zwraca obiekt reprezentujący numer kontrolki wymiany odebranego konta integracji.</span><span class="sxs-lookup"><span data-stu-id="bdec3-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="bdec3-107">To polecenie cmdlet pozwala zaktualizować stan przetwarzania wiadomości otrzymanego dla konta integracji z numerem kontrolki wymiany.</span><span class="sxs-lookup"><span data-stu-id="bdec3-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="bdec3-108">Możesz zaktualizować numer kontroli wymiany odebranego konta integracji, określając nazwę konta integracji, nazwę grupy zasobów, nazwę umowy, wartość numeru i stan przetwarzania wiadomości.</span><span class="sxs-lookup"><span data-stu-id="bdec3-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="bdec3-109">Za pomocą tego polecenia nie można utworzyć nowego konta integracji otrzymanego numeru kontroli wymiany.</span><span class="sxs-lookup"><span data-stu-id="bdec3-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="bdec3-110">Aby użyć parametrów dynamicznych, po prostu wpisz je w poleceniu lub wpisz znak łącznika(-) w celu wskazania nazwy parametru, a następnie naciskaj klawisz TAB, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="bdec3-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bdec3-111">Jeśli przegapisz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="bdec3-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="bdec3-112">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="bdec3-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="bdec3-113">Podaj parametr "-AgreementType", aby określić, czy mają być zwracane numery kontrolek X12, czy Edifact.</span><span class="sxs-lookup"><span data-stu-id="bdec3-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="bdec3-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bdec3-114">EXAMPLES</span></span>

### <span data-ttu-id="bdec3-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bdec3-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="bdec3-116">To polecenie aktualizuje numer kontroli wymiany X12 otrzymanego konta integracji dla konkretnej umowy konta integracji oraz wartość ze stanem przetwarzania wiadomości nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="bdec3-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="bdec3-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bdec3-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="bdec3-118">To polecenie aktualizuje numer kontrolki wymiany Edifact otrzymanego dla konta integracji i wartość z błędem przetwarzania wiadomości.</span><span class="sxs-lookup"><span data-stu-id="bdec3-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="bdec3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdec3-119">PARAMETERS</span></span>

### <span data-ttu-id="bdec3-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="bdec3-120">-AgreementName</span></span>
<span data-ttu-id="bdec3-121">Nazwa umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="bdec3-121">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec3-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="bdec3-122">-AgreementType</span></span>
<span data-ttu-id="bdec3-123">Typ umowy konta integracji (X12 lub Edifact).</span><span class="sxs-lookup"><span data-stu-id="bdec3-123">The integration account agreement type (X12 or Edifact).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec3-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="bdec3-124">-ControlNumberValue</span></span>
<span data-ttu-id="bdec3-125">Wartość numeru kontrolki konta integracji.</span><span class="sxs-lookup"><span data-stu-id="bdec3-125">The integration account control number value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdec3-126">-DefaultProfile</span></span>
<span data-ttu-id="bdec3-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="bdec3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdec3-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="bdec3-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="bdec3-129">Stan przetwarzania odebranych wiadomości.</span><span class="sxs-lookup"><span data-stu-id="bdec3-129">The received message processing status.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec3-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bdec3-130">-Name</span></span>
<span data-ttu-id="bdec3-131">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="bdec3-131">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdec3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdec3-132">-ResourceGroupName</span></span>
<span data-ttu-id="bdec3-133">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="bdec3-133">The integration account resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdec3-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdec3-134">-Confirm</span></span>
<span data-ttu-id="bdec3-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bdec3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdec3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdec3-136">-WhatIf</span></span>
<span data-ttu-id="bdec3-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdec3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdec3-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bdec3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdec3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdec3-139">CommonParameters</span></span>
<span data-ttu-id="bdec3-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdec3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdec3-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdec3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdec3-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdec3-142">INPUTS</span></span>

### <span data-ttu-id="bdec3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="bdec3-143">System.String</span></span>

## <span data-ttu-id="bdec3-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdec3-144">OUTPUTS</span></span>

### <span data-ttu-id="bdec3-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="bdec3-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="bdec3-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bdec3-146">NOTES</span></span>

## <span data-ttu-id="bdec3-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdec3-147">RELATED LINKS</span></span>

<span data-ttu-id="bdec3-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="bdec3-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
