---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: f222f075ec80162324d7ebcacfb4569371b59741
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553191"
---
# <span data-ttu-id="bace6-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bace6-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="bace6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bace6-102">SYNOPSIS</span></span>
<span data-ttu-id="bace6-103">Zatrzymuje zbieranie niestandardowych dzienników z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="bace6-103">Stops collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bace6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bace6-104">SYNTAX</span></span>

### <span data-ttu-id="bace6-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bace6-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bace6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bace6-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bace6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bace6-107">DESCRIPTION</span></span>
<span data-ttu-id="bace6-108">Polecenie cmdlet **disable-AzureRmOperationalInsightsLinuxCustomLogCollection** zatrzymuje zbieranie niestandardowych dzienników z połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bace6-108">The **Disable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="bace6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bace6-109">EXAMPLES</span></span>

## <span data-ttu-id="bace6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bace6-110">PARAMETERS</span></span>

### <span data-ttu-id="bace6-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bace6-111">-ResourceGroupName</span></span>
<span data-ttu-id="bace6-112">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="bace6-112">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bace6-113">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="bace6-113">-Workspace</span></span>
<span data-ttu-id="bace6-114">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bace6-114">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bace6-115">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="bace6-115">-WorkspaceName</span></span>
<span data-ttu-id="bace6-116">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bace6-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bace6-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bace6-117">-Confirm</span></span>
<span data-ttu-id="bace6-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bace6-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bace6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bace6-119">-WhatIf</span></span>
<span data-ttu-id="bace6-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bace6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bace6-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bace6-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bace6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bace6-122">-DefaultProfile</span></span>
<span data-ttu-id="bace6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bace6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bace6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bace6-124">CommonParameters</span></span>
<span data-ttu-id="bace6-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bace6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bace6-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bace6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bace6-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bace6-127">INPUTS</span></span>

### <span data-ttu-id="bace6-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bace6-128">PSWorkspace</span></span>
<span data-ttu-id="bace6-129">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="bace6-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="bace6-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bace6-130">OUTPUTS</span></span>

### <span data-ttu-id="bace6-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bace6-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bace6-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bace6-132">NOTES</span></span>
* <span data-ttu-id="bace6-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="bace6-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="bace6-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bace6-134">RELATED LINKS</span></span>

[<span data-ttu-id="bace6-135">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bace6-135">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


