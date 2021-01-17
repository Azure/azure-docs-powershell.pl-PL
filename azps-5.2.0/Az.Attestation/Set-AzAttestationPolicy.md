---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353278"
---
# <span data-ttu-id="0966f-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="0966f-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="0966f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0966f-102">SYNOPSIS</span></span>
<span data-ttu-id="0966f-103">Ustawia zasady od dzierżawy na platformie Azure Attestationn.</span><span class="sxs-lookup"><span data-stu-id="0966f-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="0966f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0966f-104">SYNTAX</span></span>

### <span data-ttu-id="0966f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0966f-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0966f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0966f-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0966f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0966f-107">DESCRIPTION</span></span>
<span data-ttu-id="0966f-108">Polecenie cmdlet Set-AzAttestationPolicy ustawia zasady od dzierżawy w zaświadczeniu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0966f-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="0966f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0966f-109">EXAMPLES</span></span>

### <span data-ttu-id="0966f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0966f-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="0966f-111">Ustawia zasady zdefiniowane przez użytkownika dla TEE typu *SgxEnclave* dla dostawcy zaświadczania *pshtest* przy użyciu formatu zasad tekstowych (domyślnie).</span><span class="sxs-lookup"><span data-stu-id="0966f-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="0966f-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0966f-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="0966f-113">Ustawia zasady zdefiniowane przez użytkownika dla TEE typu *SgxEnclave* dla dostawcy zaświadczania *pshtest* przy użyciu formatu zasad JWT.</span><span class="sxs-lookup"><span data-stu-id="0966f-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="0966f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0966f-114">PARAMETERS</span></span>

### <span data-ttu-id="0966f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0966f-115">-DefaultProfile</span></span>
<span data-ttu-id="0966f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0966f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0966f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0966f-117">-Name</span></span>
<span data-ttu-id="0966f-118">Określa nazwę dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="0966f-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="0966f-119">To polecenie cmdlet ustawia zasady zaświadczania dla dzierżawy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="0966f-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="0966f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0966f-120">-PassThru</span></span>
<span data-ttu-id="0966f-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="0966f-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0966f-122">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="0966f-122">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0966f-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="0966f-123">-Policy</span></span>
<span data-ttu-id="0966f-124">Określa dokument zasad, który należy ustawić.</span><span class="sxs-lookup"><span data-stu-id="0966f-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="0966f-125">Format zasad może być zarówno tekstowy, jak i tokenem w sieci Web JSON (JWT).</span><span class="sxs-lookup"><span data-stu-id="0966f-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="0966f-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="0966f-126">-PolicyFormat</span></span>
<span data-ttu-id="0966f-127">Określa format zasady: text lub JWT (token internetowy JSON).</span><span class="sxs-lookup"><span data-stu-id="0966f-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="0966f-128">Domyślnym formatem zasad jest tekst.</span><span class="sxs-lookup"><span data-stu-id="0966f-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="0966f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0966f-129">-ResourceGroupName</span></span>
<span data-ttu-id="0966f-130">Określa nazwę grupy zasobów dla dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="0966f-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="0966f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0966f-131">-ResourceId</span></span>
<span data-ttu-id="0966f-132">Określa identyfikator zasobu dostawcy zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="0966f-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="0966f-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="0966f-133">-Tee</span></span>
<span data-ttu-id="0966f-134">Określa typ zaufanego środowiska wykonywania.</span><span class="sxs-lookup"><span data-stu-id="0966f-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="0966f-135">Obsługiwane są cztery typy środowiska: SgxEnclave, OpenEnclave, CyResComponent i VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="0966f-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="0966f-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0966f-136">-Confirm</span></span>
<span data-ttu-id="0966f-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0966f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0966f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0966f-138">-WhatIf</span></span>
<span data-ttu-id="0966f-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0966f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0966f-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0966f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0966f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0966f-141">CommonParameters</span></span>
<span data-ttu-id="0966f-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0966f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0966f-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0966f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0966f-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0966f-144">INPUTS</span></span>

### <span data-ttu-id="0966f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0966f-145">System.String</span></span>

## <span data-ttu-id="0966f-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0966f-146">OUTPUTS</span></span>

### <span data-ttu-id="0966f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0966f-147">System.String</span></span>

## <span data-ttu-id="0966f-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0966f-148">NOTES</span></span>

## <span data-ttu-id="0966f-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0966f-149">RELATED LINKS</span></span>
