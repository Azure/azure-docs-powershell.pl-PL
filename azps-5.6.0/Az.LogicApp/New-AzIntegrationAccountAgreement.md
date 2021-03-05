---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 82fb412cca4642881ff6a84ede1f2c722c6d5086
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008842"
---
# <span data-ttu-id="958aa-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="958aa-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="958aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="958aa-102">SYNOPSIS</span></span>
<span data-ttu-id="958aa-103">Tworzy umowę na konto integracji.</span><span class="sxs-lookup"><span data-stu-id="958aa-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="958aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="958aa-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="958aa-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="958aa-105">DESCRIPTION</span></span>
<span data-ttu-id="958aa-106">Polecenie **cmdlet New-AzIntegrationAccountAgreement** tworzy umowę na konto integracji.</span><span class="sxs-lookup"><span data-stu-id="958aa-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="958aa-107">To polecenie cmdlet zwraca obiekt reprezentujący umowę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="958aa-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="958aa-108">Określ nazwę konta integracji, nazwę grupy zasobów, nazwę umowy, typ, nazwę partnera, kwalifikatorów partnera i zawartość umowy.</span><span class="sxs-lookup"><span data-stu-id="958aa-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="958aa-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="958aa-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="958aa-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="958aa-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="958aa-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="958aa-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="958aa-112">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="958aa-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="958aa-113">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="958aa-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="958aa-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="958aa-114">EXAMPLES</span></span>

### <span data-ttu-id="958aa-115">Przykład 1. Tworzenie umowy o koncie integracji</span><span class="sxs-lookup"><span data-stu-id="958aa-115">Example 1: Create a integration account agreement</span></span>
```powershell
PS C:\>New-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN

                         . . .
```

<span data-ttu-id="958aa-116">To polecenie tworzy umowę konta integracji w określonej grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="958aa-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="958aa-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="958aa-117">Example 2</span></span>

<span data-ttu-id="958aa-118">Tworzy umowę na konto integracji.</span><span class="sxs-lookup"><span data-stu-id="958aa-118">Creates an integration account agreement.</span></span> <span data-ttu-id="958aa-119">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="958aa-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="958aa-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="958aa-120">PARAMETERS</span></span>

### <span data-ttu-id="958aa-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="958aa-121">-AgreementContent</span></span>
<span data-ttu-id="958aa-122">Określa zawartość umowy w formacie JSON (JavaScript Object Notation) dla umowy.</span><span class="sxs-lookup"><span data-stu-id="958aa-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="958aa-123">Określ ten parametr lub *parametr AgreementContentFilePath.*</span><span class="sxs-lookup"><span data-stu-id="958aa-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958aa-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="958aa-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="958aa-125">Określa ścieżkę pliku zawartości umowy dla umowy.</span><span class="sxs-lookup"><span data-stu-id="958aa-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="958aa-126">Określ ten parametr lub *parametr AgreementContent.*</span><span class="sxs-lookup"><span data-stu-id="958aa-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958aa-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="958aa-127">-AgreementName</span></span>
<span data-ttu-id="958aa-128">Określa nazwę umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="958aa-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="958aa-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="958aa-129">-AgreementType</span></span>
<span data-ttu-id="958aa-130">Określa typ umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="958aa-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="958aa-131">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="958aa-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="958aa-132">X12</span><span class="sxs-lookup"><span data-stu-id="958aa-132">X12</span></span> 
- <span data-ttu-id="958aa-133">AS2</span><span class="sxs-lookup"><span data-stu-id="958aa-133">AS2</span></span>
- <span data-ttu-id="958aa-134">Edifact</span><span class="sxs-lookup"><span data-stu-id="958aa-134">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958aa-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958aa-135">-DefaultProfile</span></span>
<span data-ttu-id="958aa-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="958aa-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="958aa-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="958aa-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="958aa-138">Określa kwalifikator tożsamości biznesowej nazwy dla partnera gościa.</span><span class="sxs-lookup"><span data-stu-id="958aa-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="958aa-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="958aa-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="958aa-140">Wartość kwalifikatora tożsamości gościa w umowie integracji.</span><span class="sxs-lookup"><span data-stu-id="958aa-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="958aa-141">- GuestPartner</span><span class="sxs-lookup"><span data-stu-id="958aa-141">-GuestPartner</span></span>
<span data-ttu-id="958aa-142">Określa nazwę partnera gościa.</span><span class="sxs-lookup"><span data-stu-id="958aa-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="958aa-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="958aa-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="958aa-144">Określa kwalifikator tożsamości biznesowej nazwy partnera hosta.</span><span class="sxs-lookup"><span data-stu-id="958aa-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="958aa-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="958aa-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="958aa-146">Wartość kwalifikatora tożsamości hosta umowy integracji.</span><span class="sxs-lookup"><span data-stu-id="958aa-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="958aa-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="958aa-147">-HostPartner</span></span>
<span data-ttu-id="958aa-148">Określa nazwę partnera hosta.</span><span class="sxs-lookup"><span data-stu-id="958aa-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="958aa-149">— Metadane</span><span class="sxs-lookup"><span data-stu-id="958aa-149">-Metadata</span></span>
<span data-ttu-id="958aa-150">Określa obiekt metadanych dla umowy.</span><span class="sxs-lookup"><span data-stu-id="958aa-150">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958aa-151">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="958aa-151">-Name</span></span>
<span data-ttu-id="958aa-152">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="958aa-152">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958aa-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="958aa-153">-ResourceGroupName</span></span>
<span data-ttu-id="958aa-154">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="958aa-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="958aa-155">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="958aa-155">-Confirm</span></span>
<span data-ttu-id="958aa-156">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="958aa-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="958aa-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="958aa-157">-WhatIf</span></span>
<span data-ttu-id="958aa-158">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="958aa-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="958aa-159">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="958aa-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="958aa-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958aa-160">CommonParameters</span></span>
<span data-ttu-id="958aa-161">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="958aa-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958aa-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="958aa-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958aa-163">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="958aa-163">INPUTS</span></span>

### <span data-ttu-id="958aa-164">System.String</span><span class="sxs-lookup"><span data-stu-id="958aa-164">System.String</span></span>

## <span data-ttu-id="958aa-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="958aa-165">OUTPUTS</span></span>

### <span data-ttu-id="958aa-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="958aa-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="958aa-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="958aa-167">NOTES</span></span>

## <span data-ttu-id="958aa-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="958aa-168">RELATED LINKS</span></span>

[<span data-ttu-id="958aa-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="958aa-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="958aa-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="958aa-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="958aa-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="958aa-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


