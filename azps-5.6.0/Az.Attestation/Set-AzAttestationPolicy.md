---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c32a9e2fd474578c8526c8352e8649cb84d8b016
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966785"
---
# <span data-ttu-id="14fd5-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="14fd5-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="14fd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="14fd5-103">Ustawia zasady od dzierżawy w usłudze Azure Attestationn.</span><span class="sxs-lookup"><span data-stu-id="14fd5-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="14fd5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14fd5-104">SYNTAX</span></span>

### <span data-ttu-id="14fd5-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fd5-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14fd5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fd5-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14fd5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="14fd5-107">DESCRIPTION</span></span>
<span data-ttu-id="14fd5-108">Polecenie Set-AzAttestationPolicy ustawia zasady od dzierżawy w usługach Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="14fd5-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="14fd5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14fd5-109">EXAMPLES</span></span>

### <span data-ttu-id="14fd5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14fd5-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="14fd5-111">Ustawia zasady zdefiniowane przez użytkownika dla typu *TEE SgxEnlawe* dla testu *pshtestu* dostawcy atestacji przy użyciu formatu zasad tekstowych (ustawienie domyślne).</span><span class="sxs-lookup"><span data-stu-id="14fd5-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="14fd5-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="14fd5-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="14fd5-113">Ustawia zasady zdefiniowane przez użytkownika dla typu TEE *SgxEnlawe* dla testu *pshtestu* dostawcy atestacji przy użyciu formatu zasad JWT.</span><span class="sxs-lookup"><span data-stu-id="14fd5-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="14fd5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14fd5-114">PARAMETERS</span></span>

### <span data-ttu-id="14fd5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14fd5-115">-DefaultProfile</span></span>
<span data-ttu-id="14fd5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14fd5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14fd5-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="14fd5-117">-Name</span></span>
<span data-ttu-id="14fd5-118">Określa nazwę dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="14fd5-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="14fd5-119">To polecenie cmdlet ustawia zasady atestacji dla dzierżawy, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="14fd5-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="14fd5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14fd5-120">-PassThru</span></span>
<span data-ttu-id="14fd5-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="14fd5-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="14fd5-122">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="14fd5-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="14fd5-123">— Zasady</span><span class="sxs-lookup"><span data-stu-id="14fd5-123">-Policy</span></span>
<span data-ttu-id="14fd5-124">Określa dokument zasad do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="14fd5-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="14fd5-125">Formatem zasad może być tekst lub token sieci Web JSON (JWT).</span><span class="sxs-lookup"><span data-stu-id="14fd5-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="14fd5-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="14fd5-126">-PolicyFormat</span></span>
<span data-ttu-id="14fd5-127">Określa format zasad— tekst lub JWT (token sieci Web JSON).</span><span class="sxs-lookup"><span data-stu-id="14fd5-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="14fd5-128">Domyślnym formatem zasad jest Tekst.</span><span class="sxs-lookup"><span data-stu-id="14fd5-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="14fd5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14fd5-129">-ResourceGroupName</span></span>
<span data-ttu-id="14fd5-130">Określa nazwę grupy zasobów dostawcy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="14fd5-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="14fd5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14fd5-131">-ResourceId</span></span>
<span data-ttu-id="14fd5-132">Określa wartość ResourceID dostawcy atestacji.</span><span class="sxs-lookup"><span data-stu-id="14fd5-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="14fd5-133">- Tee</span><span class="sxs-lookup"><span data-stu-id="14fd5-133">-Tee</span></span>
<span data-ttu-id="14fd5-134">Określa typ zaufanego środowiska wykonywania.</span><span class="sxs-lookup"><span data-stu-id="14fd5-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="14fd5-135">Obsługiwane są cztery typy środowiska: SgxEnenae, OpenEnenae, CyResComponent i VBSEnżdże.</span><span class="sxs-lookup"><span data-stu-id="14fd5-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="14fd5-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14fd5-136">-Confirm</span></span>
<span data-ttu-id="14fd5-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="14fd5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14fd5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14fd5-138">-WhatIf</span></span>
<span data-ttu-id="14fd5-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14fd5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14fd5-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="14fd5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14fd5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14fd5-141">CommonParameters</span></span>
<span data-ttu-id="14fd5-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14fd5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14fd5-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14fd5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14fd5-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14fd5-144">INPUTS</span></span>

### <span data-ttu-id="14fd5-145">System.String</span><span class="sxs-lookup"><span data-stu-id="14fd5-145">System.String</span></span>

## <span data-ttu-id="14fd5-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14fd5-146">OUTPUTS</span></span>

### <span data-ttu-id="14fd5-147">System.String</span><span class="sxs-lookup"><span data-stu-id="14fd5-147">System.String</span></span>

## <span data-ttu-id="14fd5-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14fd5-148">NOTES</span></span>

## <span data-ttu-id="14fd5-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14fd5-149">RELATED LINKS</span></span>
