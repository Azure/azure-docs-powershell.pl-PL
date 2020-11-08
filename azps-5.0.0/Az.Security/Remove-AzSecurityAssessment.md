---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225695"
---
# <span data-ttu-id="39dea-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="39dea-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="39dea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39dea-102">SYNOPSIS</span></span>
<span data-ttu-id="39dea-103">Umożliwia usunięcie wyniku oceny zabezpieczeń z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="39dea-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="39dea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39dea-104">SYNTAX</span></span>

### <span data-ttu-id="39dea-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="39dea-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39dea-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="39dea-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39dea-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="39dea-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39dea-108">Inputobject</span><span class="sxs-lookup"><span data-stu-id="39dea-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39dea-109">Opis</span><span class="sxs-lookup"><span data-stu-id="39dea-109">DESCRIPTION</span></span>
<span data-ttu-id="39dea-110">Umożliwia usunięcie wyniku oceny zabezpieczeń z subskrypcji, zwykle stosowanego w przypadku usunięcia resoruce lub gdy ocena nie jest odpowiednia dla konkretnego zasobu.</span><span class="sxs-lookup"><span data-stu-id="39dea-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="39dea-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39dea-111">EXAMPLES</span></span>

### <span data-ttu-id="39dea-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39dea-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="39dea-113">Usuwanie wyniku oceny subskrypcji</span><span class="sxs-lookup"><span data-stu-id="39dea-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="39dea-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39dea-114">PARAMETERS</span></span>

### <span data-ttu-id="39dea-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="39dea-115">-AssessedResourceId</span></span>
<span data-ttu-id="39dea-116">Pełny identyfikator zasobu, dla którego jest obliczana Ocena.</span><span class="sxs-lookup"><span data-stu-id="39dea-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="39dea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39dea-117">-DefaultProfile</span></span>
<span data-ttu-id="39dea-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39dea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39dea-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="39dea-119">-InputObject</span></span>
<span data-ttu-id="39dea-120">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="39dea-120">Input Object.</span></span>

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

### <span data-ttu-id="39dea-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="39dea-121">-Name</span></span>
<span data-ttu-id="39dea-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="39dea-122">Resource name.</span></span>

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

### <span data-ttu-id="39dea-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39dea-123">-PassThru</span></span>
<span data-ttu-id="39dea-124">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="39dea-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="39dea-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39dea-125">-ResourceId</span></span>
<span data-ttu-id="39dea-126">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="39dea-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="39dea-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39dea-127">-Confirm</span></span>
<span data-ttu-id="39dea-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39dea-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39dea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39dea-129">-WhatIf</span></span>
<span data-ttu-id="39dea-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39dea-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39dea-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="39dea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39dea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39dea-132">CommonParameters</span></span>
<span data-ttu-id="39dea-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39dea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39dea-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39dea-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39dea-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39dea-135">INPUTS</span></span>

### <span data-ttu-id="39dea-136">System. String</span><span class="sxs-lookup"><span data-stu-id="39dea-136">System.String</span></span>

### <span data-ttu-id="39dea-137">Microsoft. Azure. Commands. Security. MODELES. oceny. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="39dea-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="39dea-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39dea-138">OUTPUTS</span></span>

### <span data-ttu-id="39dea-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39dea-139">System.Boolean</span></span>

## <span data-ttu-id="39dea-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39dea-140">NOTES</span></span>

## <span data-ttu-id="39dea-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39dea-141">RELATED LINKS</span></span>
