---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 997e1150549ac219c54e42fdd4c7674cd53d5ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706848"
---
# <span data-ttu-id="980e8-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="980e8-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="980e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="980e8-102">SYNOPSIS</span></span>
<span data-ttu-id="980e8-103">Usuwa zaświadczenie.</span><span class="sxs-lookup"><span data-stu-id="980e8-103">Deletes an attestation.</span></span>

## <span data-ttu-id="980e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="980e8-104">SYNTAX</span></span>

### <span data-ttu-id="980e8-105">ByAvailableAttestation (domyślny)</span><span class="sxs-lookup"><span data-stu-id="980e8-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="980e8-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="980e8-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="980e8-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="980e8-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="980e8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="980e8-108">DESCRIPTION</span></span>
<span data-ttu-id="980e8-109">Polecenie cmdlet Remove-AzAttestation usuwa określoną zaświadczenie.</span><span class="sxs-lookup"><span data-stu-id="980e8-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="980e8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="980e8-110">EXAMPLES</span></span>

### <span data-ttu-id="980e8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="980e8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name example -ResourceGroupName rg1 
```

<span data-ttu-id="980e8-112">Usuń zaświadczenie "przykład" z bieżącego abonamentu i grupy zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="980e8-112">Delete Attestation "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="980e8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="980e8-113">PARAMETERS</span></span>

### <span data-ttu-id="980e8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="980e8-114">-AsJob</span></span>
<span data-ttu-id="980e8-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="980e8-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="980e8-116">-DefaultProfile</span></span>
<span data-ttu-id="980e8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="980e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980e8-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="980e8-118">-InputObject</span></span>
<span data-ttu-id="980e8-119">Obiekt zaświadczania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="980e8-119">Attestation object to be deleted.</span></span>

```yaml
Type: PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="980e8-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="980e8-120">-Name</span></span>
<span data-ttu-id="980e8-121">Określa nazwę zaświadczenia, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="980e8-121">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980e8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="980e8-122">-PassThru</span></span>
<span data-ttu-id="980e8-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="980e8-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="980e8-124">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="980e8-124">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980e8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="980e8-125">-ResourceGroupName</span></span>
<span data-ttu-id="980e8-126">Określa nazwę grupy zasobów na potrzeby zaświadczania usługi Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="980e8-126">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980e8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="980e8-127">-ResourceId</span></span>
<span data-ttu-id="980e8-128">Identyfikator zasobu zaświadczania.</span><span class="sxs-lookup"><span data-stu-id="980e8-128">Attestation Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="980e8-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="980e8-129">-Confirm</span></span>
<span data-ttu-id="980e8-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="980e8-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980e8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="980e8-131">-WhatIf</span></span>
<span data-ttu-id="980e8-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="980e8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="980e8-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="980e8-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980e8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="980e8-134">CommonParameters</span></span>
<span data-ttu-id="980e8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="980e8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="980e8-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="980e8-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="980e8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="980e8-137">INPUTS</span></span>

### <span data-ttu-id="980e8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="980e8-138">System.String</span></span>

### <span data-ttu-id="980e8-139">Microsoft. Azure. Commands. zaświadczanie. modele. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="980e8-139">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="980e8-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="980e8-140">OUTPUTS</span></span>

### <span data-ttu-id="980e8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="980e8-141">System.Boolean</span></span>

## <span data-ttu-id="980e8-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="980e8-142">NOTES</span></span>

## <span data-ttu-id="980e8-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="980e8-143">RELATED LINKS</span></span>
