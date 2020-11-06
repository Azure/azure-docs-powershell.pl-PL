---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 5f25ec9f3b180f6bb0379b399cdbf1a96f9d1f30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552763"
---
# <span data-ttu-id="c475a-101">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c475a-101">Set-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="c475a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c475a-102">SYNOPSIS</span></span>
<span data-ttu-id="c475a-103">Aktualizuje konto integracyjne otrzymano numer kontrolki wymiany (ICN) w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c475a-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c475a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c475a-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c475a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c475a-105">DESCRIPTION</span></span>
<span data-ttu-id="c475a-106">Polecenie cmdlet Set-AzureRmIntegrationAccountGeneratedIcn aktualizuje istniejące konto integracyjne o numerze wymiany (ICN) i zwraca obiekt reprezentujący konto integracji otrzyma numer kontrolny wymiany.</span><span class="sxs-lookup"><span data-stu-id="c475a-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="c475a-107">Użyj tego polecenia cmdlet, aby zaktualizować konto usługi integracyjnej z wyświetlonym stanem przetwarzania wiadomości numeru kontrolnego wymiany.</span><span class="sxs-lookup"><span data-stu-id="c475a-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="c475a-108">Możesz zaktualizować konto integracyjne otrzymano numer kontrolny wymiany, określając nazwę konta integracji, nazwę grupy zasobów, nazwę umowy, wartość numeru kontrolki i stan przetwarzania wiadomości.</span><span class="sxs-lookup"><span data-stu-id="c475a-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="c475a-109">Za pomocą tego polecenia nie można utworzyć nowego numeru kontrolnego integracji z tym kontem.</span><span class="sxs-lookup"><span data-stu-id="c475a-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="c475a-110">Aby użyć parametrów dynamicznych, wystarczy wpisać je w poleceniu lub wpisać znak łącznika (-), aby wskazać nazwę parametru, a następnie wielokrotnie nacisnąć klawisz TAB, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="c475a-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c475a-111">Jeśli nie potrafisz wymaganego parametru szablonu, polecenie cmdlet wyświetli monit o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="c475a-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="c475a-112">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="c475a-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="c475a-113">Podaj parametr "-Agreementtype", aby określić, czy numery kontrolek X12 lub EDIFACT mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="c475a-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="c475a-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c475a-114">EXAMPLES</span></span>

### <span data-ttu-id="c475a-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c475a-115">Example 1</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="c475a-116">To polecenie powoduje zaktualizowanie konta integracji otrzymano numer kontrolki wymiany X12 dla konkretnej umowy dotyczącej konta integracji oraz wartości, dla których stan przetwarzania wiadomości nie powiódł się.</span><span class="sxs-lookup"><span data-stu-id="c475a-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="c475a-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c475a-117">Example 2</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="c475a-118">To polecenie powoduje zaktualizowanie konta integracji otrzymano numer kontrolki wymiany EDIFACT dla konkretnej umowy dotyczącej konta integracji oraz wartości, dla których stan przetwarzania wiadomości nie powiódł się.</span><span class="sxs-lookup"><span data-stu-id="c475a-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="c475a-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c475a-119">PARAMETERS</span></span>

### <span data-ttu-id="c475a-120">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="c475a-120">-AgreementName</span></span>
<span data-ttu-id="c475a-121">Nazwa umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c475a-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="c475a-122">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="c475a-122">-AgreementType</span></span>
<span data-ttu-id="c475a-123">Umowa dotycząca konta integracji (X12 lub EDIFACT).</span><span class="sxs-lookup"><span data-stu-id="c475a-123">The integration account agreement type (X12 or Edifact).</span></span>

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

### <span data-ttu-id="c475a-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="c475a-124">-ControlNumberValue</span></span>
<span data-ttu-id="c475a-125">Wartość numeru kontrolnego konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c475a-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="c475a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c475a-126">-DefaultProfile</span></span>
<span data-ttu-id="c475a-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c475a-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c475a-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="c475a-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="c475a-129">Odebrany stan przetwarzania wiadomości.</span><span class="sxs-lookup"><span data-stu-id="c475a-129">The received message processing status.</span></span>

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

### <span data-ttu-id="c475a-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c475a-130">-Name</span></span>
<span data-ttu-id="c475a-131">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c475a-131">The integration account name.</span></span>

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

### <span data-ttu-id="c475a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c475a-132">-ResourceGroupName</span></span>
<span data-ttu-id="c475a-133">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c475a-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="c475a-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c475a-134">-Confirm</span></span>
<span data-ttu-id="c475a-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c475a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c475a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c475a-136">-WhatIf</span></span>
<span data-ttu-id="c475a-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c475a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c475a-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c475a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c475a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c475a-139">CommonParameters</span></span>
<span data-ttu-id="c475a-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c475a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c475a-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c475a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c475a-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c475a-142">INPUTS</span></span>

### <span data-ttu-id="c475a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c475a-143">System.String</span></span>

## <span data-ttu-id="c475a-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c475a-144">OUTPUTS</span></span>

### <span data-ttu-id="c475a-145">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="c475a-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="c475a-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c475a-146">NOTES</span></span>

## <span data-ttu-id="c475a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c475a-147">RELATED LINKS</span></span>

<span data-ttu-id="c475a-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="c475a-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span></span>
