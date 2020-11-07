---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 44f5ffd63f2bb89f2e26d8ded6a0c7f64181bf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719443"
---
# <span data-ttu-id="aa0c7-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="aa0c7-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="aa0c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa0c7-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0c7-103">Zatrzymuje zbieranie dzienników programu IIS na komputerach.</span><span class="sxs-lookup"><span data-stu-id="aa0c7-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa0c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa0c7-104">SYNTAX</span></span>

### <span data-ttu-id="aa0c7-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa0c7-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa0c7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="aa0c7-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa0c7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aa0c7-107">DESCRIPTION</span></span>
<span data-ttu-id="aa0c7-108">Polecenie cmdlet **disable-AzureRmOperationalInsightsIISLogCollection** zatrzymuje zbieranie dzienników internetowych usług informacyjnych (IIS) z połączonych komputerów w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="aa0c7-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="aa0c7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa0c7-109">EXAMPLES</span></span>

## <span data-ttu-id="aa0c7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa0c7-110">PARAMETERS</span></span>

### <span data-ttu-id="aa0c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0c7-111">-DefaultProfile</span></span>
<span data-ttu-id="aa0c7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="aa0c7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa0c7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0c7-113">-ResourceGroupName</span></span>
<span data-ttu-id="aa0c7-114">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="aa0c7-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="aa0c7-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="aa0c7-115">-Workspace</span></span>
<span data-ttu-id="aa0c7-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa0c7-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="aa0c7-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="aa0c7-117">-WorkspaceName</span></span>
<span data-ttu-id="aa0c7-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa0c7-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="aa0c7-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa0c7-119">-Confirm</span></span>
<span data-ttu-id="aa0c7-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa0c7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa0c7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa0c7-121">-WhatIf</span></span>
<span data-ttu-id="aa0c7-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa0c7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa0c7-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa0c7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa0c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0c7-124">CommonParameters</span></span>
<span data-ttu-id="aa0c7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa0c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0c7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa0c7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0c7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa0c7-127">INPUTS</span></span>

### <span data-ttu-id="aa0c7-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="aa0c7-128">PSWorkspace</span></span>
<span data-ttu-id="aa0c7-129">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="aa0c7-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="aa0c7-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa0c7-130">OUTPUTS</span></span>

### <span data-ttu-id="aa0c7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="aa0c7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="aa0c7-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa0c7-132">NOTES</span></span>
* <span data-ttu-id="aa0c7-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="aa0c7-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="aa0c7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa0c7-134">RELATED LINKS</span></span>

[<span data-ttu-id="aa0c7-135">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="aa0c7-135">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


