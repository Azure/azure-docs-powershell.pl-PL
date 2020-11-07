---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 68264ac0e0346405ee43bfb5dc876d48be9b4d9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705056"
---
# <span data-ttu-id="f2b6f-101">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f2b6f-101">Get-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="f2b6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b6f-103">Umożliwia wyświetlenie umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-103">Gets an integration account agreement.</span></span>

## <span data-ttu-id="f2b6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2b6f-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2b6f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2b6f-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b6f-106">Polecenie cmdlet **Get-AzIntegrationAccountAgreement** pobiera umowę dotyczącą konta integracji z grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-106">The **Get-AzIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="f2b6f-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę umowy.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="f2b6f-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f2b6f-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f2b6f-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f2b6f-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f2b6f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2b6f-112">EXAMPLES</span></span>

### <span data-ttu-id="f2b6f-113">Przykład 1: uzyskiwanie umowy dotyczącej konta integracji</span><span class="sxs-lookup"><span data-stu-id="f2b6f-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
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

<span data-ttu-id="f2b6f-114">To polecenie uzyskuje umowę dotyczącą konta integracji o nazwie IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="f2b6f-115">Przykład 2: pobieranie umów dotyczących kont integracji według nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f2b6f-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="f2b6f-116">To polecenie umożliwia pobieranie umów dotyczących konta integracji według nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="f2b6f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2b6f-117">PARAMETERS</span></span>

### <span data-ttu-id="f2b6f-118">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="f2b6f-118">-AgreementName</span></span>
<span data-ttu-id="f2b6f-119">Określa nazwę umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="f2b6f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b6f-120">-DefaultProfile</span></span>
<span data-ttu-id="f2b6f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f2b6f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2b6f-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2b6f-122">-Name</span></span>
<span data-ttu-id="f2b6f-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="f2b6f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2b6f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f2b6f-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f2b6f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b6f-126">CommonParameters</span></span>
<span data-ttu-id="f2b6f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b6f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b6f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b6f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2b6f-129">INPUTS</span></span>

### <span data-ttu-id="f2b6f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f2b6f-130">System.String</span></span>

## <span data-ttu-id="f2b6f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2b6f-131">OUTPUTS</span></span>

### <span data-ttu-id="f2b6f-132">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f2b6f-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="f2b6f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2b6f-133">NOTES</span></span>

## <span data-ttu-id="f2b6f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2b6f-134">RELATED LINKS</span></span>

[<span data-ttu-id="f2b6f-135">Nowe — AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f2b6f-135">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="f2b6f-136">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f2b6f-136">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="f2b6f-137">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f2b6f-137">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


