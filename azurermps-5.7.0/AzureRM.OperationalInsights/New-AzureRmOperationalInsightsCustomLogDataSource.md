---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: 510148c5d700c1378b0e468bbd5e8a9206491284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554101"
---
# <span data-ttu-id="8ab22-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="8ab22-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="8ab22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ab22-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab22-103">Definiuje niestandardowe zasady zbierania dziennika.</span><span class="sxs-lookup"><span data-stu-id="8ab22-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ab22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ab22-104">SYNTAX</span></span>

### <span data-ttu-id="8ab22-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8ab22-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab22-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8ab22-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ab22-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8ab22-107">DESCRIPTION</span></span>
<span data-ttu-id="8ab22-108">Polecenie cmdlet **New-AzureRmOperationalInsightsCustomLogDataSource** definiuje niestandardowe zasady zbierania dziennika.</span><span class="sxs-lookup"><span data-stu-id="8ab22-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="8ab22-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ab22-109">EXAMPLES</span></span>

## <span data-ttu-id="8ab22-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ab22-110">PARAMETERS</span></span>

### <span data-ttu-id="8ab22-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="8ab22-111">-CustomLogRawJson</span></span>
<span data-ttu-id="8ab22-112">Określa niestandardową zasadę zbierania danych w postaci nieprzetworzonego ciągu JSON (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="8ab22-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab22-113">-DefaultProfile</span></span>
<span data-ttu-id="8ab22-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8ab22-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ab22-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8ab22-115">-Force</span></span>
<span data-ttu-id="8ab22-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8ab22-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ab22-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ab22-117">-Name</span></span>
<span data-ttu-id="8ab22-118">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="8ab22-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="8ab22-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ab22-119">-ResourceGroupName</span></span>
<span data-ttu-id="8ab22-120">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="8ab22-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="8ab22-121">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="8ab22-121">-Workspace</span></span>
<span data-ttu-id="8ab22-122">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ab22-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8ab22-123">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="8ab22-123">-WorkspaceName</span></span>
<span data-ttu-id="8ab22-124">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ab22-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8ab22-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ab22-125">-Confirm</span></span>
<span data-ttu-id="8ab22-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ab22-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ab22-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ab22-127">-WhatIf</span></span>
<span data-ttu-id="8ab22-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ab22-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ab22-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ab22-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ab22-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab22-130">CommonParameters</span></span>
<span data-ttu-id="8ab22-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ab22-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab22-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ab22-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab22-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ab22-133">INPUTS</span></span>

### <span data-ttu-id="8ab22-134">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8ab22-134">PSWorkspace</span></span>
<span data-ttu-id="8ab22-135">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="8ab22-135">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="8ab22-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ab22-136">OUTPUTS</span></span>

### <span data-ttu-id="8ab22-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="8ab22-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8ab22-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ab22-138">NOTES</span></span>

## <span data-ttu-id="8ab22-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ab22-139">RELATED LINKS</span></span>

[<span data-ttu-id="8ab22-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="8ab22-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="8ab22-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="8ab22-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


