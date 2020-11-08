---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: 8f06713ab61ca423fee031f8dca9df90b941ed32
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051702"
---
# <span data-ttu-id="2a731-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="2a731-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="2a731-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a731-102">SYNOPSIS</span></span>
<span data-ttu-id="2a731-103">Usuwa zaufanego podpisującego zasady dla dzierżawy w zaświadczeniu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2a731-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="2a731-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a731-104">SYNTAX</span></span>

### <span data-ttu-id="2a731-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a731-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a731-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a731-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a731-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2a731-107">DESCRIPTION</span></span>
<span data-ttu-id="2a731-108">Polecenie cmdlet Remove-AzAttestationPolicySigner powoduje usunięcie osoby podpisującej zaufane zasady dla dzierżawy w zaświadczeniu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2a731-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="2a731-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a731-109">EXAMPLES</span></span>

### <span data-ttu-id="2a731-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a731-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="2a731-111">Usuwanie zaufanej osoby podpisującej dla dostawcy zaświadczania o nazwie *pshtest*.</span><span class="sxs-lookup"><span data-stu-id="2a731-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="2a731-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a731-112">PARAMETERS</span></span>

### <span data-ttu-id="2a731-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a731-113">-DefaultProfile</span></span>
<span data-ttu-id="2a731-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a731-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a731-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a731-115">-Name</span></span>
<span data-ttu-id="2a731-116">Określa nazwę dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="2a731-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="2a731-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a731-117">-ResourceGroupName</span></span>
<span data-ttu-id="2a731-118">Określa nazwę grupy zasobów dla dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="2a731-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="2a731-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a731-119">-ResourceId</span></span>
<span data-ttu-id="2a731-120">Określa identyfikator zasobu dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="2a731-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="2a731-121">-Osoba podpisująca</span><span class="sxs-lookup"><span data-stu-id="2a731-121">-Signer</span></span>
<span data-ttu-id="2a731-122">Określa token sieci Web JSON usługi RFC7519 zawierający oświadczenie o nazwie "AAS-policyCertificate", którego wartość jest kluczem sieci Web JSON usługi RFC7517, który zawiera zaufany klucz podpisywania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2a731-122">Specifies the RFC7519 JSON Web Token containing a claim named "aas-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="2a731-123">RFC7519 JWT musi być podpisany jednym z istniejących zaufanych kluczy podpisywania.</span><span class="sxs-lookup"><span data-stu-id="2a731-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="2a731-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a731-124">-Confirm</span></span>
<span data-ttu-id="2a731-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a731-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a731-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a731-126">-WhatIf</span></span>
<span data-ttu-id="2a731-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a731-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a731-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a731-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a731-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a731-129">CommonParameters</span></span>
<span data-ttu-id="2a731-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a731-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a731-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a731-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a731-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a731-132">INPUTS</span></span>

### <span data-ttu-id="2a731-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2a731-133">System.String</span></span>

## <span data-ttu-id="2a731-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a731-134">OUTPUTS</span></span>

### <span data-ttu-id="2a731-135">Microsoft. Azure. Commands. zaświadczanie. modele. PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="2a731-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="2a731-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a731-136">NOTES</span></span>

## <span data-ttu-id="2a731-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a731-137">RELATED LINKS</span></span>
