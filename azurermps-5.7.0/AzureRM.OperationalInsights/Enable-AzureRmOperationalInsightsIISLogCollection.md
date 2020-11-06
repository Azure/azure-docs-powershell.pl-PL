---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 417bc080d707c3da02dd8a0083fb707f79d0a999
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545507"
---
# <span data-ttu-id="40d42-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="40d42-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="40d42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40d42-102">SYNOPSIS</span></span>
<span data-ttu-id="40d42-103">Rozpoczyna zbieranie dzienników programu IIS z komputerów w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="40d42-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40d42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40d42-104">SYNTAX</span></span>

### <span data-ttu-id="40d42-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="40d42-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d42-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="40d42-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d42-107">Opis</span><span class="sxs-lookup"><span data-stu-id="40d42-107">DESCRIPTION</span></span>
<span data-ttu-id="40d42-108">Polecenie cmdlet **enable-AzureRmOperationalInsightsIISLogCollection** rozpoczyna zbieranie dzienników internetowych usług informacyjnych (IIS) z połączonych komputerów w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="40d42-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="40d42-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40d42-109">EXAMPLES</span></span>

## <span data-ttu-id="40d42-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40d42-110">PARAMETERS</span></span>

### <span data-ttu-id="40d42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d42-111">-DefaultProfile</span></span>
<span data-ttu-id="40d42-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="40d42-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40d42-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d42-113">-ResourceGroupName</span></span>
<span data-ttu-id="40d42-114">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="40d42-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="40d42-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="40d42-115">-Workspace</span></span>
<span data-ttu-id="40d42-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d42-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="40d42-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="40d42-117">-WorkspaceName</span></span>
<span data-ttu-id="40d42-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d42-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="40d42-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40d42-119">-Confirm</span></span>
<span data-ttu-id="40d42-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d42-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d42-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d42-121">-WhatIf</span></span>
<span data-ttu-id="40d42-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d42-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d42-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="40d42-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d42-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d42-124">CommonParameters</span></span>
<span data-ttu-id="40d42-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d42-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d42-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d42-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d42-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40d42-127">INPUTS</span></span>

### <span data-ttu-id="40d42-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="40d42-128">PSWorkspace</span></span>
<span data-ttu-id="40d42-129">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="40d42-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="40d42-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40d42-130">OUTPUTS</span></span>

### <span data-ttu-id="40d42-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="40d42-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="40d42-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40d42-132">NOTES</span></span>

## <span data-ttu-id="40d42-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40d42-133">RELATED LINKS</span></span>

[<span data-ttu-id="40d42-134">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="40d42-134">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


