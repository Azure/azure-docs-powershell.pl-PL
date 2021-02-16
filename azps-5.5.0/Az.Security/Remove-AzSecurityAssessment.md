---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242354"
---
# <span data-ttu-id="dd880-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="dd880-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="dd880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd880-102">SYNOPSIS</span></span>
<span data-ttu-id="dd880-103">Usuwa wynik oceny zabezpieczeń z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dd880-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="dd880-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd880-104">SYNTAX</span></span>

### <span data-ttu-id="dd880-105">SubscriptionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="dd880-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd880-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="dd880-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd880-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd880-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd880-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="dd880-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd880-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd880-109">DESCRIPTION</span></span>
<span data-ttu-id="dd880-110">Usuwa z subskrypcji wynik oceny zabezpieczeń, zazwyczaj używany w przypadku usunięcia ponownego wywrzenia lub gdy ocena nie jest już istotny dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="dd880-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="dd880-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd880-111">EXAMPLES</span></span>

### <span data-ttu-id="dd880-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd880-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="dd880-113">Usuwa wynik oceny w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dd880-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="dd880-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd880-114">PARAMETERS</span></span>

### <span data-ttu-id="dd880-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="dd880-115">-AssessedResourceId</span></span>
<span data-ttu-id="dd880-116">Pełny identyfikator zasobu, na podstawie których jest obliczana ocena.</span><span class="sxs-lookup"><span data-stu-id="dd880-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd880-117">-DefaultProfile</span></span>
<span data-ttu-id="dd880-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd880-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd880-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd880-119">-InputObject</span></span>
<span data-ttu-id="dd880-120">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="dd880-120">Input Object.</span></span>

```yaml
Type: PSSecurityAssessment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dd880-121">-Name</span></span>
<span data-ttu-id="dd880-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="dd880-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd880-123">-PassThru</span></span>
<span data-ttu-id="dd880-124">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="dd880-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="dd880-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd880-125">-ResourceId</span></span>
<span data-ttu-id="dd880-126">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="dd880-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd880-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd880-127">-Confirm</span></span>
<span data-ttu-id="dd880-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd880-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd880-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd880-129">-WhatIf</span></span>
<span data-ttu-id="dd880-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd880-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd880-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dd880-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd880-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd880-132">CommonParameters</span></span>
<span data-ttu-id="dd880-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd880-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd880-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd880-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd880-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd880-135">INPUTS</span></span>

### <span data-ttu-id="dd880-136">System.String</span><span class="sxs-lookup"><span data-stu-id="dd880-136">System.String</span></span>

### <span data-ttu-id="dd880-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="dd880-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="dd880-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd880-138">OUTPUTS</span></span>

### <span data-ttu-id="dd880-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd880-139">System.Boolean</span></span>

## <span data-ttu-id="dd880-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd880-140">NOTES</span></span>

## <span data-ttu-id="dd880-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd880-141">RELATED LINKS</span></span>
