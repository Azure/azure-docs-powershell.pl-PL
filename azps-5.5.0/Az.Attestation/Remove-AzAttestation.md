---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182218"
---
# <span data-ttu-id="641e5-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="641e5-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="641e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="641e5-102">SYNOPSIS</span></span>
<span data-ttu-id="641e5-103">Usuwa atestacje.</span><span class="sxs-lookup"><span data-stu-id="641e5-103">Deletes an attestation.</span></span>

## <span data-ttu-id="641e5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="641e5-104">SYNTAX</span></span>

### <span data-ttu-id="641e5-105">ByAvailableAttastation (domyślne)</span><span class="sxs-lookup"><span data-stu-id="641e5-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="641e5-106">ResourceIdByAvailableAttastation</span><span class="sxs-lookup"><span data-stu-id="641e5-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="641e5-107">InputObjectByAvailableAttastation</span><span class="sxs-lookup"><span data-stu-id="641e5-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="641e5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="641e5-108">DESCRIPTION</span></span>
<span data-ttu-id="641e5-109">Polecenie Remove-AzAttestation cmdlet usuwa określone atestacje.</span><span class="sxs-lookup"><span data-stu-id="641e5-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="641e5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="641e5-110">EXAMPLES</span></span>

### <span data-ttu-id="641e5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="641e5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="641e5-112">Usuń dostawcę poświadczenie o nazwie *pshtest3* z grupy zasobów o nazwie *psh-test-rg* z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="641e5-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="641e5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="641e5-113">PARAMETERS</span></span>

### <span data-ttu-id="641e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="641e5-114">-DefaultProfile</span></span>
<span data-ttu-id="641e5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="641e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="641e5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="641e5-116">-InputObject</span></span>
<span data-ttu-id="641e5-117">Obiekt Attestation do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="641e5-117">Attestation object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Attestation.Models.PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="641e5-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="641e5-118">-Name</span></span>
<span data-ttu-id="641e5-119">Określa nazwę atestacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="641e5-119">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="641e5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="641e5-120">-PassThru</span></span>
<span data-ttu-id="641e5-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="641e5-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="641e5-122">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="641e5-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="641e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="641e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="641e5-124">Określa nazwę grupy zasobów dla atestacji platformy Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="641e5-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="641e5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="641e5-125">-ResourceId</span></span>
<span data-ttu-id="641e5-126">Identyfikator zasobu atestacji.</span><span class="sxs-lookup"><span data-stu-id="641e5-126">Attestation Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641e5-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="641e5-127">-Confirm</span></span>
<span data-ttu-id="641e5-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="641e5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="641e5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="641e5-129">-WhatIf</span></span>
<span data-ttu-id="641e5-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="641e5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="641e5-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="641e5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="641e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="641e5-132">CommonParameters</span></span>
<span data-ttu-id="641e5-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="641e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="641e5-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="641e5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="641e5-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="641e5-135">INPUTS</span></span>

### <span data-ttu-id="641e5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="641e5-136">System.String</span></span>

### <span data-ttu-id="641e5-137">Microsoft.Azure.Commands.Attestation.Models.PSAttastation</span><span class="sxs-lookup"><span data-stu-id="641e5-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="641e5-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="641e5-138">OUTPUTS</span></span>

### <span data-ttu-id="641e5-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="641e5-139">System.Boolean</span></span>

## <span data-ttu-id="641e5-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="641e5-140">NOTES</span></span>

## <span data-ttu-id="641e5-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="641e5-141">RELATED LINKS</span></span>
