---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234641"
---
# <span data-ttu-id="e0274-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e0274-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="e0274-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0274-102">SYNOPSIS</span></span>
<span data-ttu-id="e0274-103">Pobiera certyfikaty konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0274-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="e0274-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0274-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0274-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e0274-105">DESCRIPTION</span></span>
<span data-ttu-id="e0274-106">Polecenie cmdlet **Get-AzIntegrationAccountCertificate** pobiera certyfikaty konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0274-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="e0274-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="e0274-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="e0274-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="e0274-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e0274-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="e0274-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e0274-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="e0274-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e0274-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="e0274-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e0274-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0274-112">EXAMPLES</span></span>

### <span data-ttu-id="e0274-113">Przykład 1: Uzyskaj certyfikat konta integracyjnego</span><span class="sxs-lookup"><span data-stu-id="e0274-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="e0274-114">To polecenie pobiera certyfikat konta integracyjnego o nazwie IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="e0274-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="e0274-115">Przykład 2: uzyskiwanie certyfikatów konta integracji według nazwy konta integracji</span><span class="sxs-lookup"><span data-stu-id="e0274-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="e0274-116">To polecenie pobiera certyfikaty konta integracji dla konta integracyjnego o nazwie IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="e0274-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="e0274-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0274-117">PARAMETERS</span></span>

### <span data-ttu-id="e0274-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e0274-118">-CertificateName</span></span>
<span data-ttu-id="e0274-119">Określa nazwę certyfikatu konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="e0274-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="e0274-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0274-120">-DefaultProfile</span></span>
<span data-ttu-id="e0274-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e0274-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0274-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e0274-122">-Name</span></span>
<span data-ttu-id="e0274-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e0274-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="e0274-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0274-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0274-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0274-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e0274-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0274-126">CommonParameters</span></span>
<span data-ttu-id="e0274-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0274-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0274-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0274-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0274-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0274-129">INPUTS</span></span>

### <span data-ttu-id="e0274-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e0274-130">System.String</span></span>

## <span data-ttu-id="e0274-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0274-131">OUTPUTS</span></span>

### <span data-ttu-id="e0274-132">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e0274-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="e0274-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0274-133">NOTES</span></span>

## <span data-ttu-id="e0274-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0274-134">RELATED LINKS</span></span>

[<span data-ttu-id="e0274-135">Nowe — AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e0274-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="e0274-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e0274-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="e0274-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e0274-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


