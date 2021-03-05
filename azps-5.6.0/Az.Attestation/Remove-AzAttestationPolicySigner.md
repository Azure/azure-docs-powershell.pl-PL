---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: e0b86a1cd7c3e1355cfc760fecc257b3cde87561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966810"
---
# <span data-ttu-id="1f409-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="1f409-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="1f409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f409-102">SYNOPSIS</span></span>
<span data-ttu-id="1f409-103">Usuwa zaufanego podpiszącego zasady dla dzierżawy w usługach Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="1f409-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="1f409-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1f409-104">SYNTAX</span></span>

### <span data-ttu-id="1f409-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f409-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f409-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f409-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f409-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1f409-107">DESCRIPTION</span></span>
<span data-ttu-id="1f409-108">Polecenie Remove-AzAttestationPolicySigner cmdlet usuwa zaufanego podpiszącego zasady dla dzierżawy w atestacjach platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f409-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="1f409-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1f409-109">EXAMPLES</span></span>

### <span data-ttu-id="1f409-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1f409-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="1f409-111">Usuń zaufanego podpisatora dla dostawcy poświadczenia o nazwie *pshtest.*</span><span class="sxs-lookup"><span data-stu-id="1f409-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="1f409-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f409-112">PARAMETERS</span></span>

### <span data-ttu-id="1f409-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f409-113">-DefaultProfile</span></span>
<span data-ttu-id="1f409-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f409-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f409-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1f409-115">-Name</span></span>
<span data-ttu-id="1f409-116">Określa nazwę dostawcy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="1f409-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="1f409-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f409-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f409-118">Określa nazwę grupy zasobów dostawcy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="1f409-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="1f409-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f409-119">-ResourceId</span></span>
<span data-ttu-id="1f409-120">Określa wartość ResourceID dostawcy atestacji.</span><span class="sxs-lookup"><span data-stu-id="1f409-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="1f409-121">— Podpis</span><span class="sxs-lookup"><span data-stu-id="1f409-121">-Signer</span></span>
<span data-ttu-id="1f409-122">Określa token sieci Web JSON RFC7519 zawierający żądanie o nazwie "maa-policyCertificate", którego wartość jest kluczem sieci Web JSON JSON RFC7517 zawierającym zaufany klucz podpisywania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1f409-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="1f409-123">JWT RFC7519 musi być podpisany przy użyciu jednego z istniejących zaufanych kluczy podpisywania.</span><span class="sxs-lookup"><span data-stu-id="1f409-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="1f409-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f409-124">-Confirm</span></span>
<span data-ttu-id="1f409-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f409-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f409-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f409-126">-WhatIf</span></span>
<span data-ttu-id="1f409-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f409-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f409-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1f409-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f409-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f409-129">CommonParameters</span></span>
<span data-ttu-id="1f409-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f409-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f409-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f409-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f409-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f409-132">INPUTS</span></span>

### <span data-ttu-id="1f409-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1f409-133">System.String</span></span>

## <span data-ttu-id="1f409-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f409-134">OUTPUTS</span></span>

### <span data-ttu-id="1f409-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="1f409-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="1f409-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1f409-136">NOTES</span></span>

## <span data-ttu-id="1f409-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f409-137">RELATED LINKS</span></span>
