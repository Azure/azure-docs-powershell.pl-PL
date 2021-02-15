---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: fdd62a78b9d75ef222dc9f41f2c791afadfad9b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182202"
---
# <span data-ttu-id="5f18b-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="5f18b-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="5f18b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f18b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f18b-103">Usuwa zaufanego podpiszącego zasady dla dzierżawy w usługach Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="5f18b-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="5f18b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5f18b-104">SYNTAX</span></span>

### <span data-ttu-id="5f18b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f18b-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f18b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f18b-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f18b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5f18b-107">DESCRIPTION</span></span>
<span data-ttu-id="5f18b-108">Polecenie Remove-AzAttestationPolicySigner cmdlet usuwa zaufanego podpiszącego zasady dla dzierżawy w atestacjach platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f18b-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="5f18b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5f18b-109">EXAMPLES</span></span>

### <span data-ttu-id="5f18b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5f18b-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="5f18b-111">Usuń zaufanego podpisatora dla dostawcy poświadczenia o *nazwie pshtest.*</span><span class="sxs-lookup"><span data-stu-id="5f18b-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="5f18b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f18b-112">PARAMETERS</span></span>

### <span data-ttu-id="5f18b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f18b-113">-DefaultProfile</span></span>
<span data-ttu-id="5f18b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f18b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f18b-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5f18b-115">-Name</span></span>
<span data-ttu-id="5f18b-116">Określa nazwę dostawcy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="5f18b-116">Specifies the name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f18b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f18b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f18b-118">Określa nazwę grupy zasobów dostawcy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="5f18b-118">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f18b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f18b-119">-ResourceId</span></span>
<span data-ttu-id="5f18b-120">Określa wartość ResourceID dostawcy atestacji.</span><span class="sxs-lookup"><span data-stu-id="5f18b-120">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f18b-121">— Podpis</span><span class="sxs-lookup"><span data-stu-id="5f18b-121">-Signer</span></span>
<span data-ttu-id="5f18b-122">Określa token sieci Web JSON JSON RFC7519 zawierający żądanie o nazwie "maa-policyCertificate", którego wartość jest kluczem sieci Web JSON JSON RFC7517 zawierającym zaufany klucz podpisywania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5f18b-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="5f18b-123">JWT RFC7519 musi być podpisany przy użyciu jednego z istniejących zaufanych kluczy podpisywania.</span><span class="sxs-lookup"><span data-stu-id="5f18b-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f18b-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f18b-124">-Confirm</span></span>
<span data-ttu-id="5f18b-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5f18b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f18b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f18b-126">-WhatIf</span></span>
<span data-ttu-id="5f18b-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f18b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f18b-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5f18b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f18b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f18b-129">CommonParameters</span></span>
<span data-ttu-id="5f18b-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f18b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f18b-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f18b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f18b-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f18b-132">INPUTS</span></span>

### <span data-ttu-id="5f18b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5f18b-133">System.String</span></span>

## <span data-ttu-id="5f18b-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f18b-134">OUTPUTS</span></span>

### <span data-ttu-id="5f18b-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="5f18b-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="5f18b-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5f18b-136">NOTES</span></span>

## <span data-ttu-id="5f18b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f18b-137">RELATED LINKS</span></span>
