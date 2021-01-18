---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: f1d59a0a34072a91242c6595c269ba55c4397e0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502561"
---
# <span data-ttu-id="f5545-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f5545-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="f5545-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5545-102">SYNOPSIS</span></span>
<span data-ttu-id="f5545-103">Dodaje uwierzytelnione konto, które będzie używane dla żądań polecenia cmdlet serwera usług Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="f5545-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="f5545-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5545-104">SYNTAX</span></span>

### <span data-ttu-id="f5545-105">UserParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f5545-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5545-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f5545-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5545-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f5545-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5545-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f5545-108">DESCRIPTION</span></span>
<span data-ttu-id="f5545-109">Polecenie cmdlet Add-AzAnalysisServicesAccount służy do logowania się do wystąpienia serwera usługi Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f5545-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="f5545-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5545-110">EXAMPLES</span></span>

### <span data-ttu-id="f5545-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5545-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="f5545-112">W tym przykładzie zostanie dodane konto określone przez zmienną $UserCredential w środowisku usług Analysis Services westcentralus.asazure.windows.net.</span><span class="sxs-lookup"><span data-stu-id="f5545-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="f5545-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f5545-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="f5545-114">Pierwsze polecenie pobiera główne poświadczenia usługi aplikacji, a następnie zapisuje je w zmiennej $ApplicationCredential.</span><span class="sxs-lookup"><span data-stu-id="f5545-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="f5545-115">Drugie polecenie Dodaj konto główne usługi aplikacji określone przez zmienną $ApplicationCredential i dzierżawy do środowiska usług westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="f5545-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="f5545-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f5545-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="f5545-117">W tym przykładzie zostanie dodane konto główne usługi aplikacji określone przez identyfikator aplikacji dzierżawy i CertificateThumbprint do środowiska usług Analysis Services westcentralus.asazure.windows.net.</span><span class="sxs-lookup"><span data-stu-id="f5545-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="f5545-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5545-118">PARAMETERS</span></span>

### <span data-ttu-id="f5545-119">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="f5545-119">-ApplicationId</span></span>
<span data-ttu-id="f5545-120">Identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f5545-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5545-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f5545-121">-CertificateThumbprint</span></span>
<span data-ttu-id="f5545-122">Skrót certyfikatu (odcisk palca)</span><span class="sxs-lookup"><span data-stu-id="f5545-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5545-123">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="f5545-123">-Credential</span></span>
<span data-ttu-id="f5545-124">Poświadczenia logowania</span><span class="sxs-lookup"><span data-stu-id="f5545-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5545-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="f5545-125">-RolloutEnvironment</span></span>
<span data-ttu-id="f5545-126">Nazwa środowiska usług Azure Analysis Services, do którego chcesz się zalogować.</span><span class="sxs-lookup"><span data-stu-id="f5545-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="f5545-127">Uwzględniając pełną nazwę serwera, na przykład asazure://westcentralus.asazure.windows.net/testserver, prawidłową wartością tej zmiennej będzie westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="f5545-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5545-128">-Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="f5545-128">-ServicePrincipal</span></span>
<span data-ttu-id="f5545-129">Wskazuje, że to konto uwierzytelnia się, dostarczając poświadczenia podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f5545-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5545-130">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="f5545-130">-TenantId</span></span>
<span data-ttu-id="f5545-131">Nazwa lub identyfikator dzierżawy</span><span class="sxs-lookup"><span data-stu-id="f5545-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5545-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5545-132">-Confirm</span></span>
<span data-ttu-id="f5545-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5545-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5545-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5545-134">-WhatIf</span></span>
<span data-ttu-id="f5545-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5545-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5545-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f5545-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5545-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5545-137">CommonParameters</span></span>
<span data-ttu-id="f5545-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5545-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5545-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5545-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5545-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5545-140">INPUTS</span></span>

### <span data-ttu-id="f5545-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f5545-141">None</span></span>

## <span data-ttu-id="f5545-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5545-142">OUTPUTS</span></span>

### <span data-ttu-id="f5545-143">Microsoft. Azure. Commands. AnalysisServices. dataplan. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f5545-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="f5545-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5545-144">NOTES</span></span>
<span data-ttu-id="f5545-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="f5545-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="f5545-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5545-146">RELATED LINKS</span></span>
