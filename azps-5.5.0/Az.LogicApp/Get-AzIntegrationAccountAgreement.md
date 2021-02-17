---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 46cc7c75075cffface03af2ed70b5339dd36b0a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192315"
---
# <span data-ttu-id="a3b8f-101">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a3b8f-101">Get-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="a3b8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b8f-103">Otrzymuje umowę na konto integracji.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-103">Gets an integration account agreement.</span></span>

## <span data-ttu-id="a3b8f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3b8f-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3b8f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3b8f-105">DESCRIPTION</span></span>
<span data-ttu-id="a3b8f-106">Polecenie **cmdlet Get-AzIntegrationAccountAgreement** otrzymuje umowę na konto integracji od grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-106">The **Get-AzIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="a3b8f-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę umowy.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="a3b8f-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a3b8f-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a3b8f-110">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a3b8f-111">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a3b8f-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3b8f-112">EXAMPLES</span></span>

### <span data-ttu-id="a3b8f-113">Przykład 1. Uzyskiwanie umowy o konto integracji</span><span class="sxs-lookup"><span data-stu-id="a3b8f-113">Example 1: Get an integration account agreement</span></span>
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

<span data-ttu-id="a3b8f-114">To polecenie otrzymuje umowę konta integracji o nazwie IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="a3b8f-115">Przykład 2. Uzyskiwanie umów dotyczących konta integracji według nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a3b8f-115">Example 2: Get integration account agreements by resource group name</span></span>
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

<span data-ttu-id="a3b8f-116">To polecenie pobiera umowy konta integracji według nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="a3b8f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3b8f-117">PARAMETERS</span></span>

### <span data-ttu-id="a3b8f-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="a3b8f-118">-AgreementName</span></span>
<span data-ttu-id="a3b8f-119">Określa nazwę umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="a3b8f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b8f-120">-DefaultProfile</span></span>
<span data-ttu-id="a3b8f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a3b8f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3b8f-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a3b8f-122">-Name</span></span>
<span data-ttu-id="a3b8f-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="a3b8f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b8f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a3b8f-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a3b8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b8f-126">CommonParameters</span></span>
<span data-ttu-id="a3b8f-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3b8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b8f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3b8f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b8f-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3b8f-129">INPUTS</span></span>

### <span data-ttu-id="a3b8f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a3b8f-130">System.String</span></span>

## <span data-ttu-id="a3b8f-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3b8f-131">OUTPUTS</span></span>

### <span data-ttu-id="a3b8f-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a3b8f-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="a3b8f-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3b8f-133">NOTES</span></span>

## <span data-ttu-id="a3b8f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3b8f-134">RELATED LINKS</span></span>

[<span data-ttu-id="a3b8f-135">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a3b8f-135">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="a3b8f-136">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a3b8f-136">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="a3b8f-137">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a3b8f-137">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


