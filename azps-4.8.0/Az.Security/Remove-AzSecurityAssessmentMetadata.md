---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222933"
---
# <span data-ttu-id="2ceaf-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="2ceaf-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="2ceaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ceaf-102">SYNOPSIS</span></span>
<span data-ttu-id="2ceaf-103">Usuwa metadane oceny zabezpieczeń z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="2ceaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ceaf-104">SYNTAX</span></span>

### <span data-ttu-id="2ceaf-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2ceaf-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ceaf-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2ceaf-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ceaf-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="2ceaf-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ceaf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2ceaf-108">DESCRIPTION</span></span>
<span data-ttu-id="2ceaf-109">Usuwa metadane oceny zabezpieczeń z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="2ceaf-110">Ta akcja spowoduje usunięcie typu oceny i wszystkich odpowiednich wyników oceny z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="2ceaf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ceaf-111">EXAMPLES</span></span>

### <span data-ttu-id="2ceaf-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ceaf-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="2ceaf-113">Usuwa typ oceny z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="2ceaf-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ceaf-114">PARAMETERS</span></span>

### <span data-ttu-id="2ceaf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ceaf-115">-DefaultProfile</span></span>
<span data-ttu-id="2ceaf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ceaf-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2ceaf-117">-InputObject</span></span>
<span data-ttu-id="2ceaf-118">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-118">Input Object.</span></span>

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

### <span data-ttu-id="2ceaf-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2ceaf-119">-Name</span></span>
<span data-ttu-id="2ceaf-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-120">Resource name.</span></span>

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

### <span data-ttu-id="2ceaf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ceaf-121">-PassThru</span></span>
<span data-ttu-id="2ceaf-122">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="2ceaf-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ceaf-123">-ResourceId</span></span>
<span data-ttu-id="2ceaf-124">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2ceaf-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ceaf-125">-Confirm</span></span>
<span data-ttu-id="2ceaf-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ceaf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ceaf-127">-WhatIf</span></span>
<span data-ttu-id="2ceaf-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ceaf-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ceaf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ceaf-130">CommonParameters</span></span>
<span data-ttu-id="2ceaf-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ceaf-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ceaf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ceaf-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ceaf-133">INPUTS</span></span>

### <span data-ttu-id="2ceaf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2ceaf-134">System.String</span></span>

### <span data-ttu-id="2ceaf-135">Microsoft. Azure. Commands. Security. models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="2ceaf-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="2ceaf-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ceaf-136">OUTPUTS</span></span>

### <span data-ttu-id="2ceaf-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ceaf-137">System.Boolean</span></span>

## <span data-ttu-id="2ceaf-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ceaf-138">NOTES</span></span>

## <span data-ttu-id="2ceaf-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ceaf-139">RELATED LINKS</span></span>
