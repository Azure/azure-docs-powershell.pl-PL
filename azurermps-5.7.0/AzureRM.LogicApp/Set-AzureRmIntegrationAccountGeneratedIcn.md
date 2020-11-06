---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 732c7cd1feb54c1475839a39f57f81d154da80ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525081"
---
# <span data-ttu-id="f45f4-101">Set-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="f45f4-101">Set-AzureRmIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="f45f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f45f4-102">SYNOPSIS</span></span>
<span data-ttu-id="f45f4-103">Umożliwia zaktualizowanie wygenerowanego numeru kontrolnego (ICN) z konta integracji w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f45f4-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f45f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f45f4-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f45f4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f45f4-105">DESCRIPTION</span></span>
<span data-ttu-id="f45f4-106">Polecenie cmdlet Set-AzureRmIntegrationAccountGeneratedIcn aktualizuje istniejący numer kontrolki wymiany (ICN) konta integracji i zwraca obiekt reprezentujący wygenerowany numer kontrolny wymiany dla konta integracji.</span><span class="sxs-lookup"><span data-stu-id="f45f4-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="f45f4-107">Użyj tego polecenia cmdlet, aby zaktualizować numer kontrolki wymiany dla konta integracji.</span><span class="sxs-lookup"><span data-stu-id="f45f4-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="f45f4-108">Numer rozliczeniowy kontroli wymiany wygenerowany przez konto integracji można zaktualizować, określając nazwę konta integracji, nazwę grupy zasobów i nazwę umowy.</span><span class="sxs-lookup"><span data-stu-id="f45f4-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="f45f4-109">Za pomocą tego polecenia nie można utworzyć nowego numeru kontrolnego wymiany dla konta integracji.</span><span class="sxs-lookup"><span data-stu-id="f45f4-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="f45f4-110">Aby użyć parametrów dynamicznych, wystarczy wpisać je w poleceniu lub wpisać znak łącznika (-), aby wskazać nazwę parametru, a następnie wielokrotnie nacisnąć klawisz TAB, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="f45f4-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f45f4-111">Jeśli nie potrafisz wymaganego parametru szablonu, polecenie cmdlet wyświetli monit o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="f45f4-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="f45f4-112">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="f45f4-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="f45f4-113">Podaj parametr "-Agreementtype", aby określić, czy numery kontrolek X12 lub EDIFACT mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="f45f4-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="f45f4-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f45f4-114">EXAMPLES</span></span>

### <span data-ttu-id="f45f4-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f45f4-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="f45f4-116">To polecenie pobiera numer X12a wymiany danych generowany przez konto integracji dla konkretnej umowy dotyczącej konta integracji, zwiększając jej wartość o 100, a następnie zapisuje zaktualizowaną wartość.</span><span class="sxs-lookup"><span data-stu-id="f45f4-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="f45f4-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f45f4-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="f45f4-118">To polecenie pobiera numer EdifactIntegrationAccountAgreementa wymiany danych generowany przez konto integracji dla konkretnej umowy dotyczącej konta integracji, zwiększając jej wartość o 100, a następnie zapisuje zaktualizowaną wartość.</span><span class="sxs-lookup"><span data-stu-id="f45f4-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="f45f4-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f45f4-119">PARAMETERS</span></span>

### <span data-ttu-id="f45f4-120">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="f45f4-120">-AgreementName</span></span>
<span data-ttu-id="f45f4-121">Nazwa umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="f45f4-121">The integration account agreement name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f45f4-122">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="f45f4-122">-AgreementType</span></span>
<span data-ttu-id="f45f4-123">Typ umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="f45f4-123">The integration account agreement type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f45f4-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="f45f4-124">-ControlNumber</span></span>
<span data-ttu-id="f45f4-125">Nowa wartość wygenerowanego numeru kontrolki.</span><span class="sxs-lookup"><span data-stu-id="f45f4-125">The generated control number new value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f45f4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45f4-126">-DefaultProfile</span></span>
<span data-ttu-id="f45f4-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f45f4-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f45f4-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f45f4-128">-Name</span></span>
<span data-ttu-id="f45f4-129">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="f45f4-129">The integration account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f45f4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f45f4-130">-ResourceGroupName</span></span>
<span data-ttu-id="f45f4-131">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="f45f4-131">The integration account resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f45f4-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f45f4-132">-Confirm</span></span>
<span data-ttu-id="f45f4-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f45f4-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f45f4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f45f4-134">-WhatIf</span></span>
<span data-ttu-id="f45f4-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f45f4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f45f4-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f45f4-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f45f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45f4-137">CommonParameters</span></span>
<span data-ttu-id="f45f4-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f45f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45f4-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f45f4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45f4-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f45f4-140">INPUTS</span></span>

### <span data-ttu-id="f45f4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f45f4-141">System.String</span></span>

## <span data-ttu-id="f45f4-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f45f4-142">OUTPUTS</span></span>

### <span data-ttu-id="f45f4-143">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="f45f4-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="f45f4-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f45f4-144">NOTES</span></span>

## <span data-ttu-id="f45f4-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f45f4-145">RELATED LINKS</span></span>

[<span data-ttu-id="f45f4-146">Get-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="f45f4-146">Get-AzureRmIntegrationAccountGeneratedIcn</span></span>](./Get-AzureRmIntegrationAccountGeneratedIcn.md)

