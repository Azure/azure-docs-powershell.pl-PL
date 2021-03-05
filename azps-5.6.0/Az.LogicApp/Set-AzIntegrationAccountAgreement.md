---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 6c7781f5617571003083328adfac8aa7b349841b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962938"
---
# <span data-ttu-id="94946-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="94946-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="94946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94946-102">SYNOPSIS</span></span>
<span data-ttu-id="94946-103">Modyfikuje umowę na konto integracji.</span><span class="sxs-lookup"><span data-stu-id="94946-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="94946-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94946-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94946-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="94946-105">DESCRIPTION</span></span>
<span data-ttu-id="94946-106">Polecenie **cmdlet Set-AzIntegrationAccountAgreement** modyfikuje umowę na konto integracji.</span><span class="sxs-lookup"><span data-stu-id="94946-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="94946-107">To polecenie cmdlet zwraca obiekt reprezentujący umowę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="94946-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="94946-108">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę umowy.</span><span class="sxs-lookup"><span data-stu-id="94946-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="94946-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="94946-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="94946-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="94946-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="94946-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="94946-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="94946-112">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="94946-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="94946-113">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="94946-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="94946-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94946-114">EXAMPLES</span></span>

### <span data-ttu-id="94946-115">Przykład 1. Aktualizowanie umowy konta integracji</span><span class="sxs-lookup"><span data-stu-id="94946-115">Example 1: Update an integration account agreement</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="94946-116">To polecenie aktualizuje umowę konta integracji w określonej grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94946-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="94946-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="94946-117">Example 2</span></span>

<span data-ttu-id="94946-118">Modyfikuje umowę na konto integracji.</span><span class="sxs-lookup"><span data-stu-id="94946-118">Modifies an integration account agreement.</span></span> <span data-ttu-id="94946-119">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="94946-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountAgreement -AgreementContentFilePath 'C:\temp\AgreementContent.json' -AgreementName 'IntegrationAccountAgreement06' -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Metadata <Object> -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="94946-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94946-120">PARAMETERS</span></span>

### <span data-ttu-id="94946-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="94946-121">-AgreementContent</span></span>
<span data-ttu-id="94946-122">Określa zawartość umowy w formacie JSON (JavaScript Object Notation) dla umowy.</span><span class="sxs-lookup"><span data-stu-id="94946-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="94946-123">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="94946-123">-AgreementContentFilePath</span></span>
<span data-ttu-id="94946-124">Określa ścieżkę pliku zawartości umowy dla umowy.</span><span class="sxs-lookup"><span data-stu-id="94946-124">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="94946-125">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="94946-125">-AgreementName</span></span>
<span data-ttu-id="94946-126">Określa nazwę umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="94946-126">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="94946-127">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="94946-127">-AgreementType</span></span>
<span data-ttu-id="94946-128">Określa typ umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="94946-128">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="94946-129">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="94946-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94946-130">X12</span><span class="sxs-lookup"><span data-stu-id="94946-130">X12</span></span> 
- <span data-ttu-id="94946-131">AS2</span><span class="sxs-lookup"><span data-stu-id="94946-131">AS2</span></span>
- <span data-ttu-id="94946-132">Edifact</span><span class="sxs-lookup"><span data-stu-id="94946-132">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94946-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94946-133">-DefaultProfile</span></span>
<span data-ttu-id="94946-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="94946-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94946-135">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="94946-135">-Force</span></span>
<span data-ttu-id="94946-136">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="94946-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94946-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="94946-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="94946-138">Określa kwalifikator tożsamości biznesowej nazwy dla partnera gościa.</span><span class="sxs-lookup"><span data-stu-id="94946-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="94946-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="94946-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="94946-140">Wartość kwalifikatora tożsamości gościa w umowie integracji.</span><span class="sxs-lookup"><span data-stu-id="94946-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="94946-141">- GuestPartner</span><span class="sxs-lookup"><span data-stu-id="94946-141">-GuestPartner</span></span>
<span data-ttu-id="94946-142">Określa nazwę partnera gościa.</span><span class="sxs-lookup"><span data-stu-id="94946-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="94946-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="94946-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="94946-144">Określa kwalifikator tożsamości biznesowej nazwy partnera hosta.</span><span class="sxs-lookup"><span data-stu-id="94946-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="94946-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="94946-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="94946-146">Wartość kwalifikatora tożsamości hosta umowy integracji.</span><span class="sxs-lookup"><span data-stu-id="94946-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="94946-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="94946-147">-HostPartner</span></span>
<span data-ttu-id="94946-148">Określa nazwę partnera hosta.</span><span class="sxs-lookup"><span data-stu-id="94946-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="94946-149">— Metadane</span><span class="sxs-lookup"><span data-stu-id="94946-149">-Metadata</span></span>
<span data-ttu-id="94946-150">Określa obiekt metadanych dla umowy.</span><span class="sxs-lookup"><span data-stu-id="94946-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="94946-151">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="94946-151">-Name</span></span>
<span data-ttu-id="94946-152">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="94946-152">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="94946-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94946-153">-ResourceGroupName</span></span>
<span data-ttu-id="94946-154">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94946-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="94946-155">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94946-155">-Confirm</span></span>
<span data-ttu-id="94946-156">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94946-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94946-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94946-157">-WhatIf</span></span>
<span data-ttu-id="94946-158">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94946-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94946-159">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94946-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94946-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94946-160">CommonParameters</span></span>
<span data-ttu-id="94946-161">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94946-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94946-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94946-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94946-163">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94946-163">INPUTS</span></span>

### <span data-ttu-id="94946-164">System.String</span><span class="sxs-lookup"><span data-stu-id="94946-164">System.String</span></span>

## <span data-ttu-id="94946-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94946-165">OUTPUTS</span></span>

### <span data-ttu-id="94946-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="94946-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="94946-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94946-167">NOTES</span></span>

## <span data-ttu-id="94946-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94946-168">RELATED LINKS</span></span>

[<span data-ttu-id="94946-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="94946-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="94946-170">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="94946-170">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="94946-171">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="94946-171">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


