---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 4c91ced490226901a45e0eacb7caa204daa20558
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976810"
---
# <span data-ttu-id="d679e-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="d679e-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="d679e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d679e-102">SYNOPSIS</span></span>
<span data-ttu-id="d679e-103">Aktualizuje numer ICN (Interchange Control Number) wygenerowany dla konta integracji w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d679e-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="d679e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d679e-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d679e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d679e-105">DESCRIPTION</span></span>
<span data-ttu-id="d679e-106">Polecenie Set-AzIntegrationAccountGeneratedIcn aktualizuje numer istniejącej kontrolki wymiany wygenerowanego konta integracji (ICN) i zwraca obiekt reprezentujący numer kontrolki wygenerowanej na koncie integracji.</span><span class="sxs-lookup"><span data-stu-id="d679e-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="d679e-107">To polecenie cmdlet pozwala zaktualizować numer kontrolki wymiany wygenerowany na koncie integracji.</span><span class="sxs-lookup"><span data-stu-id="d679e-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="d679e-108">Możesz zaktualizować numer kontroli wymiany wygenerowanego dla konta integracji, określając nazwę konta integracji, nazwę grupy zasobów i nazwę umowy.</span><span class="sxs-lookup"><span data-stu-id="d679e-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="d679e-109">Za pomocą tego polecenia nie można utworzyć nowego konta integracji wygenerowanego numeru kontroli wymiany.</span><span class="sxs-lookup"><span data-stu-id="d679e-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="d679e-110">Aby użyć parametrów dynamicznych, po prostu wpisz je w poleceniu lub wpisz znak łącznika(-) w celu wskazania nazwy parametru, a następnie naciskaj klawisz TAB, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="d679e-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d679e-111">Jeśli przegapisz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="d679e-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="d679e-112">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="d679e-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="d679e-113">Podaj parametr "-AgreementType", aby określić, czy mają być zwracane numery kontrolek X12, czy Edifact.</span><span class="sxs-lookup"><span data-stu-id="d679e-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="d679e-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d679e-114">EXAMPLES</span></span>

### <span data-ttu-id="d679e-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d679e-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="d679e-116">To polecenie pobiera numer kontrolki wymiany X12 wygenerowanego na koncie integracji dla konkretnej umowy konta integracji, zwiększa wartość o 100, a następnie zapisuje zaktualizowaną wartość.</span><span class="sxs-lookup"><span data-stu-id="d679e-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="d679e-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d679e-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="d679e-118">To polecenie pobiera numer kontroli wymiany EdifactIntegrationAccountAgreement dla konkretnego konta integracji, zwiększa jego wartość o 100, a następnie zapisuje zaktualizowaną wartość.</span><span class="sxs-lookup"><span data-stu-id="d679e-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="d679e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d679e-119">PARAMETERS</span></span>

### <span data-ttu-id="d679e-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="d679e-120">-AgreementName</span></span>
<span data-ttu-id="d679e-121">Nazwa umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d679e-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="d679e-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="d679e-122">-AgreementType</span></span>
<span data-ttu-id="d679e-123">Typ umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d679e-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="d679e-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="d679e-124">-ControlNumber</span></span>
<span data-ttu-id="d679e-125">Wygenerowana kontrolka numeruje nową wartość.</span><span class="sxs-lookup"><span data-stu-id="d679e-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="d679e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d679e-126">-DefaultProfile</span></span>
<span data-ttu-id="d679e-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d679e-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d679e-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d679e-128">-Name</span></span>
<span data-ttu-id="d679e-129">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d679e-129">The integration account name.</span></span>

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

### <span data-ttu-id="d679e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d679e-130">-ResourceGroupName</span></span>
<span data-ttu-id="d679e-131">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d679e-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="d679e-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d679e-132">-Confirm</span></span>
<span data-ttu-id="d679e-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d679e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d679e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d679e-134">-WhatIf</span></span>
<span data-ttu-id="d679e-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d679e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d679e-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d679e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d679e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d679e-137">CommonParameters</span></span>
<span data-ttu-id="d679e-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d679e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d679e-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d679e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d679e-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d679e-140">INPUTS</span></span>

### <span data-ttu-id="d679e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d679e-141">System.String</span></span>

## <span data-ttu-id="d679e-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d679e-142">OUTPUTS</span></span>

### <span data-ttu-id="d679e-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="d679e-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="d679e-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d679e-144">NOTES</span></span>

## <span data-ttu-id="d679e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d679e-145">RELATED LINKS</span></span>

[<span data-ttu-id="d679e-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="d679e-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

