---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: c825e77706a3f7efba3efac1e29866a8a296464b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527521"
---
# <span data-ttu-id="a99d6-101">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a99d6-101">Get-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="a99d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a99d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a99d6-103">Umożliwia wyświetlenie umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a99d6-103">Gets an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a99d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a99d6-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a99d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a99d6-105">DESCRIPTION</span></span>
<span data-ttu-id="a99d6-106">Polecenie cmdlet **Get-AzureRmIntegrationAccountAgreement** pobiera umowę dotyczącą konta integracji z grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a99d6-106">The **Get-AzureRmIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="a99d6-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę umowy.</span><span class="sxs-lookup"><span data-stu-id="a99d6-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="a99d6-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="a99d6-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a99d6-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="a99d6-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a99d6-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="a99d6-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a99d6-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="a99d6-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a99d6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a99d6-112">EXAMPLES</span></span>

### <span data-ttu-id="a99d6-113">Przykład 1: uzyskiwanie umowy dotyczącej konta integracji</span><span class="sxs-lookup"><span data-stu-id="a99d6-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="a99d6-114">To polecenie uzyskuje umowę dotyczącą konta integracji o nazwie IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="a99d6-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="a99d6-115">Przykład 2: pobieranie umów dotyczących kont integracji według nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a99d6-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="a99d6-116">To polecenie umożliwia pobieranie umów dotyczących konta integracji według nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a99d6-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="a99d6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a99d6-117">PARAMETERS</span></span>

### <span data-ttu-id="a99d6-118">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="a99d6-118">-AgreementName</span></span>
<span data-ttu-id="a99d6-119">Określa nazwę umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a99d6-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="a99d6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a99d6-120">-Name</span></span>
<span data-ttu-id="a99d6-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a99d6-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a99d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="a99d6-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a99d6-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99d6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99d6-124">-DefaultProfile</span></span>
<span data-ttu-id="a99d6-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a99d6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a99d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99d6-126">CommonParameters</span></span>
<span data-ttu-id="a99d6-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a99d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99d6-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99d6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99d6-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a99d6-129">INPUTS</span></span>

## <span data-ttu-id="a99d6-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a99d6-130">OUTPUTS</span></span>

### <span data-ttu-id="a99d6-131">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a99d6-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="a99d6-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a99d6-132">NOTES</span></span>

## <span data-ttu-id="a99d6-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a99d6-133">RELATED LINKS</span></span>

[<span data-ttu-id="a99d6-134">Nowe — AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a99d6-134">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="a99d6-135">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a99d6-135">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="a99d6-136">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a99d6-136">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


