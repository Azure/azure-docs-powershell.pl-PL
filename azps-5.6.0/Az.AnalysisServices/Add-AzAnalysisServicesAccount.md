---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: 523ccfb44d29473e41560de88d34519f98272375
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015562"
---
# <span data-ttu-id="f99c6-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f99c6-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="f99c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f99c6-102">SYNOPSIS</span></span>
<span data-ttu-id="f99c6-103">Dodaje uwierzytelnione konto do użycia na potrzeby żądań cmdlet serwera usługi Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="f99c6-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="f99c6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f99c6-104">SYNTAX</span></span>

### <span data-ttu-id="f99c6-105">UserParameterSetName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f99c6-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99c6-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f99c6-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99c6-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f99c6-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f99c6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f99c6-108">DESCRIPTION</span></span>
<span data-ttu-id="f99c6-109">Polecenie Add-AzAnalysisServicesAccount cmdlet służy do logowania się do wystąpienia serwera usług Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f99c6-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="f99c6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f99c6-110">EXAMPLES</span></span>

### <span data-ttu-id="f99c6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f99c6-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="f99c6-112">W tym przykładzie konto określone przez zmienną $UserCredential do środowiska usług westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="f99c6-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="f99c6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f99c6-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="f99c6-114">Pierwsze polecenie pobiera poświadczenia podmiotu zabezpieczeń usługi aplikacji, a następnie przechowuje je w $ApplicationCredential danych.</span><span class="sxs-lookup"><span data-stu-id="f99c6-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="f99c6-115">Drugie polecenie dodaje główne konto usługi aplikacji określone przez zmienną $ApplicationCredential i TenantId do środowiska usług westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="f99c6-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="f99c6-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f99c6-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="f99c6-117">W tym przykładzie zostanie dodano główne konto usługi aplikacji określone przez wartości ApplicationId, TenantId i CertificateThumbprint do środowiska usług westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="f99c6-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="f99c6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f99c6-118">PARAMETERS</span></span>

### <span data-ttu-id="f99c6-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f99c6-119">-ApplicationId</span></span>
<span data-ttu-id="f99c6-120">Identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f99c6-120">The application ID.</span></span>

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

### <span data-ttu-id="f99c6-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f99c6-121">-CertificateThumbprint</span></span>
<span data-ttu-id="f99c6-122">Certificate Hash (Thumbprint)</span><span class="sxs-lookup"><span data-stu-id="f99c6-122">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="f99c6-123">- Credential</span><span class="sxs-lookup"><span data-stu-id="f99c6-123">-Credential</span></span>
<span data-ttu-id="f99c6-124">Poświadczenia logowania</span><span class="sxs-lookup"><span data-stu-id="f99c6-124">Login credentials</span></span>

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

### <span data-ttu-id="f99c6-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="f99c6-125">-RolloutEnvironment</span></span>
<span data-ttu-id="f99c6-126">Nazwa środowiska usług Azure Analysis Services, w którym chcesz się logować.</span><span class="sxs-lookup"><span data-stu-id="f99c6-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="f99c6-127">Przy pełnej nazwie serwera, na przykład asazure://westcentralus.asazure.windows.net/testserver, prawidłowa wartość tej zmiennej będzie westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="f99c6-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

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

### <span data-ttu-id="f99c6-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f99c6-128">-ServicePrincipal</span></span>
<span data-ttu-id="f99c6-129">Wskazuje, że to konto uwierzytelnia się, podając poświadczenia podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f99c6-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="f99c6-130">- TenantId</span><span class="sxs-lookup"><span data-stu-id="f99c6-130">-TenantId</span></span>
<span data-ttu-id="f99c6-131">Nazwa dzierżawy lub identyfikator</span><span class="sxs-lookup"><span data-stu-id="f99c6-131">Tenant name or ID</span></span>

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

### <span data-ttu-id="f99c6-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f99c6-132">-Confirm</span></span>
<span data-ttu-id="f99c6-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f99c6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f99c6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f99c6-134">-WhatIf</span></span>
<span data-ttu-id="f99c6-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f99c6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f99c6-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f99c6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f99c6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99c6-137">CommonParameters</span></span>
<span data-ttu-id="f99c6-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f99c6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99c6-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f99c6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99c6-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f99c6-140">INPUTS</span></span>

### <span data-ttu-id="f99c6-141">Brak</span><span class="sxs-lookup"><span data-stu-id="f99c6-141">None</span></span>

## <span data-ttu-id="f99c6-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f99c6-142">OUTPUTS</span></span>

### <span data-ttu-id="f99c6-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f99c6-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="f99c6-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f99c6-144">NOTES</span></span>
<span data-ttu-id="f99c6-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="f99c6-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="f99c6-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f99c6-146">RELATED LINKS</span></span>
