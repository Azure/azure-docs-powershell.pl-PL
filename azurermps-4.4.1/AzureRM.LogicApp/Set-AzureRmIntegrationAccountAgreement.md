---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: bfbcfe06acbfefefcd754a7ad541ebafe31bae7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550943"
---
# <span data-ttu-id="e93de-101">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="e93de-101">Set-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="e93de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e93de-102">SYNOPSIS</span></span>
<span data-ttu-id="e93de-103">Modyfikuje umowę dotyczącą konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e93de-103">Modifies an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e93de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e93de-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e93de-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e93de-105">DESCRIPTION</span></span>
<span data-ttu-id="e93de-106">Polecenie cmdlet **Set-AzureRmIntegrationAccountAgreement** modyfikuje umowę dotyczącą konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e93de-106">The **Set-AzureRmIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="e93de-107">To polecenie cmdlet zwraca obiekt reprezentujący umowę dotyczącą konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e93de-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="e93de-108">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę umowy.</span><span class="sxs-lookup"><span data-stu-id="e93de-108">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="e93de-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="e93de-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="e93de-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="e93de-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e93de-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="e93de-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e93de-112">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="e93de-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e93de-113">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="e93de-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e93de-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e93de-114">EXAMPLES</span></span>

### <span data-ttu-id="e93de-115">Przykład 1: aktualizowanie umowy dotyczącej konta integracji</span><span class="sxs-lookup"><span data-stu-id="e93de-115">Example 1: Update an integration account agreement</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="e93de-116">To polecenie aktualizuje umowę dotyczącą konta integracji w określonej grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e93de-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="e93de-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e93de-117">PARAMETERS</span></span>

### <span data-ttu-id="e93de-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="e93de-118">-AgreementContent</span></span>
<span data-ttu-id="e93de-119">Określa zawartość kontraktu w formacie notacji kodu JavaScript (kod JSON) dla umowy.</span><span class="sxs-lookup"><span data-stu-id="e93de-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="e93de-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="e93de-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="e93de-121">Określa ścieżkę pliku dla treści umowy.</span><span class="sxs-lookup"><span data-stu-id="e93de-121">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="e93de-122">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="e93de-122">-AgreementName</span></span>
<span data-ttu-id="e93de-123">Określa nazwę umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e93de-123">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="e93de-124">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="e93de-124">-AgreementType</span></span>
<span data-ttu-id="e93de-125">Określa typ umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e93de-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="e93de-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e93de-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e93de-127">X12</span><span class="sxs-lookup"><span data-stu-id="e93de-127">X12</span></span> 
- <span data-ttu-id="e93de-128">AS2</span><span class="sxs-lookup"><span data-stu-id="e93de-128">AS2</span></span>
- <span data-ttu-id="e93de-129">Edifact</span><span class="sxs-lookup"><span data-stu-id="e93de-129">Edifact</span></span>

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

### <span data-ttu-id="e93de-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e93de-130">-Force</span></span>
<span data-ttu-id="e93de-131">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e93de-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e93de-132">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="e93de-132">-GuestIdentityQualifier</span></span>
<span data-ttu-id="e93de-133">Określa nazwę kwalifikatora tożsamości biznesowej partnera gościa.</span><span class="sxs-lookup"><span data-stu-id="e93de-133">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="e93de-134">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="e93de-134">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="e93de-135">Wartość kwalifikatora tożsamości gościa w umowie dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e93de-135">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="e93de-136">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="e93de-136">-GuestPartner</span></span>
<span data-ttu-id="e93de-137">Określa nazwę partnera będącego gościem.</span><span class="sxs-lookup"><span data-stu-id="e93de-137">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="e93de-138">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="e93de-138">-HostIdentityQualifier</span></span>
<span data-ttu-id="e93de-139">Określa nazwę kwalifikatora tożsamości biznesowej dla partnera hosta.</span><span class="sxs-lookup"><span data-stu-id="e93de-139">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="e93de-140">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="e93de-140">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="e93de-141">Wartość kwalifikatora tożsamości hosta umowy dotyczącej konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="e93de-141">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="e93de-142">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="e93de-142">-HostPartner</span></span>
<span data-ttu-id="e93de-143">Określa nazwę partnera hosta.</span><span class="sxs-lookup"><span data-stu-id="e93de-143">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="e93de-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e93de-144">-Metadata</span></span>
<span data-ttu-id="e93de-145">Określa obiekt metadanych dla umowy.</span><span class="sxs-lookup"><span data-stu-id="e93de-145">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="e93de-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e93de-146">-Name</span></span>
<span data-ttu-id="e93de-147">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e93de-147">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="e93de-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e93de-148">-ResourceGroupName</span></span>
<span data-ttu-id="e93de-149">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e93de-149">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e93de-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e93de-150">-Confirm</span></span>
<span data-ttu-id="e93de-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e93de-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e93de-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e93de-152">-WhatIf</span></span>
<span data-ttu-id="e93de-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e93de-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e93de-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e93de-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e93de-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93de-155">-DefaultProfile</span></span>
<span data-ttu-id="e93de-156">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e93de-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e93de-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93de-157">CommonParameters</span></span>
<span data-ttu-id="e93de-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e93de-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93de-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e93de-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93de-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e93de-160">INPUTS</span></span>

## <span data-ttu-id="e93de-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e93de-161">OUTPUTS</span></span>

### <span data-ttu-id="e93de-162">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="e93de-162">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="e93de-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e93de-163">NOTES</span></span>

## <span data-ttu-id="e93de-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e93de-164">RELATED LINKS</span></span>

[<span data-ttu-id="e93de-165">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="e93de-165">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="e93de-166">Nowe — AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="e93de-166">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="e93de-167">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="e93de-167">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)


