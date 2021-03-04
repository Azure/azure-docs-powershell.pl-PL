---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: daa0d87eab24743863e6cbbcdd1c010e974c113c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974337"
---
# <span data-ttu-id="99e27-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="99e27-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="99e27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e27-102">SYNOPSIS</span></span>
<span data-ttu-id="99e27-103">Usuwa metadane oceny zabezpieczeń z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="99e27-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="99e27-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99e27-104">SYNTAX</span></span>

### <span data-ttu-id="99e27-105">SubscriptionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="99e27-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e27-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="99e27-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e27-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="99e27-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99e27-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="99e27-108">DESCRIPTION</span></span>
<span data-ttu-id="99e27-109">Usuwa metadane oceny zabezpieczeń z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="99e27-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="99e27-110">Ta czynność spowoduje usunięcie z subskrypcji typu testu i wszystkich odpowiednich wyników testów.</span><span class="sxs-lookup"><span data-stu-id="99e27-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="99e27-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99e27-111">EXAMPLES</span></span>

### <span data-ttu-id="99e27-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99e27-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="99e27-113">Usuwanie typu oceny z subskrypcji</span><span class="sxs-lookup"><span data-stu-id="99e27-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="99e27-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99e27-114">PARAMETERS</span></span>

### <span data-ttu-id="99e27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e27-115">-DefaultProfile</span></span>
<span data-ttu-id="99e27-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="99e27-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99e27-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99e27-117">-InputObject</span></span>
<span data-ttu-id="99e27-118">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="99e27-118">Input Object.</span></span>

```yaml
Type: PSSecurityAssessmentMetadata
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99e27-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="99e27-119">-Name</span></span>
<span data-ttu-id="99e27-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="99e27-120">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e27-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99e27-121">-PassThru</span></span>
<span data-ttu-id="99e27-122">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="99e27-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="99e27-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99e27-123">-ResourceId</span></span>
<span data-ttu-id="99e27-124">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="99e27-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="99e27-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99e27-125">-Confirm</span></span>
<span data-ttu-id="99e27-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99e27-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99e27-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99e27-127">-WhatIf</span></span>
<span data-ttu-id="99e27-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99e27-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99e27-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="99e27-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99e27-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e27-130">CommonParameters</span></span>
<span data-ttu-id="99e27-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e27-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e27-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99e27-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e27-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99e27-133">INPUTS</span></span>

### <span data-ttu-id="99e27-134">System.String</span><span class="sxs-lookup"><span data-stu-id="99e27-134">System.String</span></span>

### <span data-ttu-id="99e27-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="99e27-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="99e27-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99e27-136">OUTPUTS</span></span>

### <span data-ttu-id="99e27-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="99e27-137">System.Boolean</span></span>

## <span data-ttu-id="99e27-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99e27-138">NOTES</span></span>

## <span data-ttu-id="99e27-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99e27-139">RELATED LINKS</span></span>
