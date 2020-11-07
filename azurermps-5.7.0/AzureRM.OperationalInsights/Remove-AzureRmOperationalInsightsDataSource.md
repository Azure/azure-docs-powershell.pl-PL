---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: a3f650861f70ad9110f4716e5034cd5e7f930343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718631"
---
# <span data-ttu-id="260f6-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="260f6-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="260f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="260f6-102">SYNOPSIS</span></span>
<span data-ttu-id="260f6-103">Usuwa źródło danych.</span><span class="sxs-lookup"><span data-stu-id="260f6-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="260f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="260f6-104">SYNTAX</span></span>

### <span data-ttu-id="260f6-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="260f6-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="260f6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="260f6-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="260f6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="260f6-107">DESCRIPTION</span></span>
<span data-ttu-id="260f6-108">Polecenie cmdlet **Remove-AzureRmOperationalInsightsDataSource** usuwa źródło danych.</span><span class="sxs-lookup"><span data-stu-id="260f6-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="260f6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="260f6-109">EXAMPLES</span></span>

## <span data-ttu-id="260f6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="260f6-110">PARAMETERS</span></span>

### <span data-ttu-id="260f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="260f6-111">-DefaultProfile</span></span>
<span data-ttu-id="260f6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="260f6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260f6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="260f6-113">-Force</span></span>
<span data-ttu-id="260f6-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="260f6-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="260f6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="260f6-115">-Name</span></span>
<span data-ttu-id="260f6-116">Określa nazwę źródła danych, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="260f6-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="260f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="260f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="260f6-118">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="260f6-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="260f6-119">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="260f6-119">-Workspace</span></span>
<span data-ttu-id="260f6-120">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="260f6-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="260f6-121">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="260f6-121">-WorkspaceName</span></span>
<span data-ttu-id="260f6-122">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="260f6-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="260f6-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="260f6-123">-Confirm</span></span>
<span data-ttu-id="260f6-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="260f6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260f6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="260f6-125">-WhatIf</span></span>
<span data-ttu-id="260f6-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="260f6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="260f6-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="260f6-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="260f6-128">CommonParameters</span></span>
<span data-ttu-id="260f6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="260f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="260f6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="260f6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="260f6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="260f6-131">INPUTS</span></span>

### <span data-ttu-id="260f6-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="260f6-132">PSWorkspace</span></span>
<span data-ttu-id="260f6-133">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="260f6-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="260f6-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="260f6-134">OUTPUTS</span></span>

## <span data-ttu-id="260f6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="260f6-135">NOTES</span></span>
* <span data-ttu-id="260f6-136">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="260f6-136">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="260f6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="260f6-137">RELATED LINKS</span></span>

[<span data-ttu-id="260f6-138">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="260f6-138">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="260f6-139">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="260f6-139">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


