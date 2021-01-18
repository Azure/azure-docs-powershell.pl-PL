---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503018"
---
# <span data-ttu-id="9bb4e-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="9bb4e-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="9bb4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bb4e-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb4e-103">Usuwa metadane oceny zabezpieczeń z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="9bb4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bb4e-104">SYNTAX</span></span>

### <span data-ttu-id="9bb4e-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9bb4e-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb4e-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="9bb4e-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb4e-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="9bb4e-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bb4e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9bb4e-108">DESCRIPTION</span></span>
<span data-ttu-id="9bb4e-109">Usuwa metadane oceny zabezpieczeń z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="9bb4e-110">Ta akcja spowoduje usunięcie typu oceny i wszystkich odpowiednich wyników oceny z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="9bb4e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bb4e-111">EXAMPLES</span></span>

### <span data-ttu-id="9bb4e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9bb4e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="9bb4e-113">Usuwa typ oceny z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="9bb4e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bb4e-114">PARAMETERS</span></span>

### <span data-ttu-id="9bb4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb4e-115">-DefaultProfile</span></span>
<span data-ttu-id="9bb4e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bb4e-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9bb4e-117">-InputObject</span></span>
<span data-ttu-id="9bb4e-118">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-118">Input Object.</span></span>

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

### <span data-ttu-id="9bb4e-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9bb4e-119">-Name</span></span>
<span data-ttu-id="9bb4e-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-120">Resource name.</span></span>

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

### <span data-ttu-id="9bb4e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bb4e-121">-PassThru</span></span>
<span data-ttu-id="9bb4e-122">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="9bb4e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bb4e-123">-ResourceId</span></span>
<span data-ttu-id="9bb4e-124">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9bb4e-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9bb4e-125">-Confirm</span></span>
<span data-ttu-id="9bb4e-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bb4e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bb4e-127">-WhatIf</span></span>
<span data-ttu-id="9bb4e-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bb4e-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bb4e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb4e-130">CommonParameters</span></span>
<span data-ttu-id="9bb4e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bb4e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb4e-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bb4e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb4e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bb4e-133">INPUTS</span></span>

### <span data-ttu-id="9bb4e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9bb4e-134">System.String</span></span>

### <span data-ttu-id="9bb4e-135">Microsoft. Azure. Commands. Security. models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="9bb4e-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="9bb4e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bb4e-136">OUTPUTS</span></span>

### <span data-ttu-id="9bb4e-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9bb4e-137">System.Boolean</span></span>

## <span data-ttu-id="9bb4e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bb4e-138">NOTES</span></span>

## <span data-ttu-id="9bb4e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bb4e-139">RELATED LINKS</span></span>
