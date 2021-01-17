---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337282"
---
# <span data-ttu-id="b97fb-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="b97fb-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="b97fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b97fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b97fb-103">Umożliwia usunięcie wyniku oceny zabezpieczeń z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b97fb-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="b97fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b97fb-104">SYNTAX</span></span>

### <span data-ttu-id="b97fb-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b97fb-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b97fb-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="b97fb-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b97fb-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="b97fb-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b97fb-108">Inputobject</span><span class="sxs-lookup"><span data-stu-id="b97fb-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b97fb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b97fb-109">DESCRIPTION</span></span>
<span data-ttu-id="b97fb-110">Umożliwia usunięcie wyniku oceny zabezpieczeń z subskrypcji, zwykle stosowanego w przypadku usunięcia resoruce lub gdy ocena nie jest odpowiednia dla konkretnego zasobu.</span><span class="sxs-lookup"><span data-stu-id="b97fb-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="b97fb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b97fb-111">EXAMPLES</span></span>

### <span data-ttu-id="b97fb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b97fb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="b97fb-113">Usuwanie wyniku oceny subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b97fb-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="b97fb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b97fb-114">PARAMETERS</span></span>

### <span data-ttu-id="b97fb-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="b97fb-115">-AssessedResourceId</span></span>
<span data-ttu-id="b97fb-116">Pełny identyfikator zasobu, dla którego jest obliczana Ocena.</span><span class="sxs-lookup"><span data-stu-id="b97fb-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="b97fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97fb-117">-DefaultProfile</span></span>
<span data-ttu-id="b97fb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b97fb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b97fb-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b97fb-119">-InputObject</span></span>
<span data-ttu-id="b97fb-120">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="b97fb-120">Input Object.</span></span>

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

### <span data-ttu-id="b97fb-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b97fb-121">-Name</span></span>
<span data-ttu-id="b97fb-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b97fb-122">Resource name.</span></span>

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

### <span data-ttu-id="b97fb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b97fb-123">-PassThru</span></span>
<span data-ttu-id="b97fb-124">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="b97fb-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b97fb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b97fb-125">-ResourceId</span></span>
<span data-ttu-id="b97fb-126">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="b97fb-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="b97fb-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b97fb-127">-Confirm</span></span>
<span data-ttu-id="b97fb-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b97fb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b97fb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b97fb-129">-WhatIf</span></span>
<span data-ttu-id="b97fb-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b97fb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b97fb-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b97fb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b97fb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97fb-132">CommonParameters</span></span>
<span data-ttu-id="b97fb-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b97fb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97fb-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b97fb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97fb-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b97fb-135">INPUTS</span></span>

### <span data-ttu-id="b97fb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b97fb-136">System.String</span></span>

### <span data-ttu-id="b97fb-137">Microsoft. Azure. Commands. Security. MODELES. oceny. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="b97fb-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="b97fb-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b97fb-138">OUTPUTS</span></span>

### <span data-ttu-id="b97fb-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b97fb-139">System.Boolean</span></span>

## <span data-ttu-id="b97fb-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b97fb-140">NOTES</span></span>

## <span data-ttu-id="b97fb-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b97fb-141">RELATED LINKS</span></span>
