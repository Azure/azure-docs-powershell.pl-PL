---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 838191018c50856f92f82699f7ac54686f1b3d97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717518"
---
# <span data-ttu-id="46c51-101">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="46c51-101">New-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="46c51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46c51-102">SYNOPSIS</span></span>
<span data-ttu-id="46c51-103">Umożliwia utworzenie umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="46c51-103">Creates an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46c51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46c51-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46c51-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46c51-105">DESCRIPTION</span></span>
<span data-ttu-id="46c51-106">Polecenie cmdlet **New-AzureRmIntegrationAccountAgreement** umożliwia utworzenie umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="46c51-106">The **New-AzureRmIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="46c51-107">To polecenie cmdlet zwraca obiekt reprezentujący umowę dotyczącą konta integracji.</span><span class="sxs-lookup"><span data-stu-id="46c51-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="46c51-108">Określ nazwę konta integracji, nazwę grupy zasobów, nazwę umowy, typ, nazwę partnera, kwalifikatory partnera i zawartość umowy.</span><span class="sxs-lookup"><span data-stu-id="46c51-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>

<span data-ttu-id="46c51-109">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="46c51-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="46c51-110">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="46c51-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="46c51-111">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="46c51-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="46c51-112">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="46c51-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="46c51-113">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="46c51-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="46c51-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46c51-114">EXAMPLES</span></span>

### <span data-ttu-id="46c51-115">Przykład 1: Tworzenie umowy dotyczącej konta integracji</span><span class="sxs-lookup"><span data-stu-id="46c51-115">Example 1: Create a integration account agreement</span></span>
```
PS C:\>New-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="46c51-116">To polecenie tworzy umowę dotyczącą konta integracji w określonej grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="46c51-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="46c51-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46c51-117">PARAMETERS</span></span>

### <span data-ttu-id="46c51-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="46c51-118">-AgreementContent</span></span>
<span data-ttu-id="46c51-119">Określa zawartość kontraktu w formacie notacji kodu JavaScript (kod JSON) dla umowy.</span><span class="sxs-lookup"><span data-stu-id="46c51-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="46c51-120">Określ ten parametr lub parametr *AgreementContentFilePath* .</span><span class="sxs-lookup"><span data-stu-id="46c51-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c51-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="46c51-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="46c51-122">Określa ścieżkę pliku dla treści umowy.</span><span class="sxs-lookup"><span data-stu-id="46c51-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="46c51-123">Określ ten parametr lub parametr *AgreementContent* .</span><span class="sxs-lookup"><span data-stu-id="46c51-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c51-124">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="46c51-124">-AgreementName</span></span>
<span data-ttu-id="46c51-125">Określa nazwę umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="46c51-125">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="46c51-126">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="46c51-126">-AgreementType</span></span>
<span data-ttu-id="46c51-127">Określa typ umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="46c51-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="46c51-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="46c51-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46c51-129">X12</span><span class="sxs-lookup"><span data-stu-id="46c51-129">X12</span></span> 
- <span data-ttu-id="46c51-130">AS2</span><span class="sxs-lookup"><span data-stu-id="46c51-130">AS2</span></span>
- <span data-ttu-id="46c51-131">Edifact</span><span class="sxs-lookup"><span data-stu-id="46c51-131">Edifact</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c51-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c51-132">-DefaultProfile</span></span>
<span data-ttu-id="46c51-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="46c51-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46c51-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="46c51-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="46c51-135">Określa nazwę kwalifikatora tożsamości biznesowej partnera gościa.</span><span class="sxs-lookup"><span data-stu-id="46c51-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="46c51-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="46c51-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="46c51-137">Wartość kwalifikatora tożsamości gościa w umowie dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="46c51-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="46c51-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="46c51-138">-GuestPartner</span></span>
<span data-ttu-id="46c51-139">Określa nazwę partnera będącego gościem.</span><span class="sxs-lookup"><span data-stu-id="46c51-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="46c51-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="46c51-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="46c51-141">Określa nazwę kwalifikatora tożsamości biznesowej dla partnera hosta.</span><span class="sxs-lookup"><span data-stu-id="46c51-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="46c51-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="46c51-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="46c51-143">Wartość kwalifikatora tożsamości hosta umowy dotyczącej konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="46c51-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="46c51-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="46c51-144">-HostPartner</span></span>
<span data-ttu-id="46c51-145">Określa nazwę partnera hosta.</span><span class="sxs-lookup"><span data-stu-id="46c51-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="46c51-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="46c51-146">-Metadata</span></span>
<span data-ttu-id="46c51-147">Określa obiekt metadanych dla umowy.</span><span class="sxs-lookup"><span data-stu-id="46c51-147">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c51-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46c51-148">-Name</span></span>
<span data-ttu-id="46c51-149">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="46c51-149">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c51-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46c51-150">-ResourceGroupName</span></span>
<span data-ttu-id="46c51-151">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="46c51-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="46c51-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46c51-152">-Confirm</span></span>
<span data-ttu-id="46c51-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46c51-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46c51-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c51-154">-WhatIf</span></span>
<span data-ttu-id="46c51-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46c51-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46c51-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46c51-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46c51-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c51-157">CommonParameters</span></span>
<span data-ttu-id="46c51-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46c51-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c51-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46c51-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c51-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46c51-160">INPUTS</span></span>

### <span data-ttu-id="46c51-161">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="46c51-161">None</span></span>
<span data-ttu-id="46c51-162">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="46c51-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46c51-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46c51-163">OUTPUTS</span></span>

### <span data-ttu-id="46c51-164">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="46c51-164">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="46c51-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46c51-165">NOTES</span></span>

## <span data-ttu-id="46c51-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46c51-166">RELATED LINKS</span></span>

[<span data-ttu-id="46c51-167">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="46c51-167">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="46c51-168">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="46c51-168">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="46c51-169">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="46c51-169">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


