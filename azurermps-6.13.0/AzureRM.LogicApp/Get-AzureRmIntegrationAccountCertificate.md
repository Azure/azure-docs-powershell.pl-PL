---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 673c06cfd54f00a6d781d1415798e639875b7c46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719114"
---
# <span data-ttu-id="78447-101">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="78447-101">Get-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="78447-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78447-102">SYNOPSIS</span></span>
<span data-ttu-id="78447-103">Pobiera certyfikaty konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78447-103">Gets integration account certificates from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78447-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78447-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>]
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78447-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78447-105">DESCRIPTION</span></span>
<span data-ttu-id="78447-106">Polecenie cmdlet **Get-AzureRmIntegrationAccountCertificate** pobiera certyfikaty konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78447-106">The **Get-AzureRmIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="78447-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="78447-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="78447-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="78447-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="78447-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="78447-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="78447-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="78447-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="78447-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="78447-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="78447-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78447-112">EXAMPLES</span></span>

### <span data-ttu-id="78447-113">Przykład 1: Uzyskaj certyfikat konta integracyjnego</span><span class="sxs-lookup"><span data-stu-id="78447-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="78447-114">To polecenie pobiera certyfikat konta integracyjnego o nazwie IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="78447-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="78447-115">Przykład 2: uzyskiwanie certyfikatów konta integracji według nazwy konta integracji</span><span class="sxs-lookup"><span data-stu-id="78447-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="78447-116">To polecenie pobiera certyfikaty konta integracji dla konta integracyjnego o nazwie IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="78447-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="78447-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78447-117">PARAMETERS</span></span>

### <span data-ttu-id="78447-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="78447-118">-CertificateName</span></span>
<span data-ttu-id="78447-119">Określa nazwę certyfikatu konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="78447-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="78447-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78447-120">-DefaultProfile</span></span>
<span data-ttu-id="78447-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="78447-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78447-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78447-122">-Name</span></span>
<span data-ttu-id="78447-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="78447-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="78447-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78447-124">-ResourceGroupName</span></span>
<span data-ttu-id="78447-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78447-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="78447-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78447-126">CommonParameters</span></span>
<span data-ttu-id="78447-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78447-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78447-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78447-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78447-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78447-129">INPUTS</span></span>

### <span data-ttu-id="78447-130">System. String</span><span class="sxs-lookup"><span data-stu-id="78447-130">System.String</span></span>

## <span data-ttu-id="78447-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78447-131">OUTPUTS</span></span>

### <span data-ttu-id="78447-132">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="78447-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="78447-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78447-133">NOTES</span></span>

## <span data-ttu-id="78447-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78447-134">RELATED LINKS</span></span>

[<span data-ttu-id="78447-135">Nowe — AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="78447-135">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="78447-136">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="78447-136">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="78447-137">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="78447-137">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


