---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353293"
---
# <span data-ttu-id="b7142-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="b7142-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="b7142-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7142-102">SYNOPSIS</span></span>
<span data-ttu-id="b7142-103">Usuwa zaświadczenie.</span><span class="sxs-lookup"><span data-stu-id="b7142-103">Deletes an attestation.</span></span>

## <span data-ttu-id="b7142-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7142-104">SYNTAX</span></span>

### <span data-ttu-id="b7142-105">ByAvailableAttestation (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b7142-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7142-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="b7142-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7142-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="b7142-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7142-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b7142-108">DESCRIPTION</span></span>
<span data-ttu-id="b7142-109">Polecenie cmdlet Remove-AzAttestation usuwa określoną zaświadczenie.</span><span class="sxs-lookup"><span data-stu-id="b7142-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="b7142-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7142-110">EXAMPLES</span></span>

### <span data-ttu-id="b7142-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b7142-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="b7142-112">Usuń dostawcę zaświadczania o nazwie *pshtest3* w grupie zasobów o nazwie *PSH-test-RG* z bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="b7142-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="b7142-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7142-113">PARAMETERS</span></span>

### <span data-ttu-id="b7142-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7142-114">-DefaultProfile</span></span>
<span data-ttu-id="b7142-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7142-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7142-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b7142-116">-InputObject</span></span>
<span data-ttu-id="b7142-117">Obiekt zaświadczania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b7142-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="b7142-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7142-118">-Name</span></span>
<span data-ttu-id="b7142-119">Określa nazwę zaświadczenia, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="b7142-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="b7142-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7142-120">-PassThru</span></span>
<span data-ttu-id="b7142-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="b7142-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b7142-122">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="b7142-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b7142-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7142-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7142-124">Określa nazwę grupy zasobów na potrzeby zaświadczania usługi Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b7142-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="b7142-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7142-125">-ResourceId</span></span>
<span data-ttu-id="b7142-126">Identyfikator zasobu zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="b7142-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="b7142-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7142-127">-Confirm</span></span>
<span data-ttu-id="b7142-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7142-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7142-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7142-129">-WhatIf</span></span>
<span data-ttu-id="b7142-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7142-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7142-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7142-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7142-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7142-132">CommonParameters</span></span>
<span data-ttu-id="b7142-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7142-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7142-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7142-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7142-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7142-135">INPUTS</span></span>

### <span data-ttu-id="b7142-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b7142-136">System.String</span></span>

### <span data-ttu-id="b7142-137">Microsoft. Azure. Commands. zaświadczanie. modele. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="b7142-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="b7142-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7142-138">OUTPUTS</span></span>

### <span data-ttu-id="b7142-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7142-139">System.Boolean</span></span>

## <span data-ttu-id="b7142-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7142-140">NOTES</span></span>

## <span data-ttu-id="b7142-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7142-141">RELATED LINKS</span></span>
