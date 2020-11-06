---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 0b907f07280eae32ecb208fd13195767145c9541
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550856"
---
# <span data-ttu-id="cb662-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="cb662-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="cb662-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb662-102">SYNOPSIS</span></span>
<span data-ttu-id="cb662-103">Rozpoczyna zbieranie niestandardowych dzienników z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="cb662-103">Starts collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb662-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb662-104">SYNTAX</span></span>

### <span data-ttu-id="cb662-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cb662-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb662-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cb662-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb662-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cb662-107">DESCRIPTION</span></span>
<span data-ttu-id="cb662-108">Polecenie cmdlet **enable-AzureRmOperationalInsightsLinuxCustomLogCollection** rozpoczyna zbieranie niestandardowych dzienników z połączonych komputerów Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="cb662-108">The **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="cb662-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb662-109">EXAMPLES</span></span>

## <span data-ttu-id="cb662-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb662-110">PARAMETERS</span></span>

### <span data-ttu-id="cb662-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb662-111">-ResourceGroupName</span></span>
<span data-ttu-id="cb662-112">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="cb662-112">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="cb662-113">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="cb662-113">-Workspace</span></span>
<span data-ttu-id="cb662-114">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb662-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cb662-115">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="cb662-115">-WorkspaceName</span></span>
<span data-ttu-id="cb662-116">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb662-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cb662-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb662-117">-Confirm</span></span>
<span data-ttu-id="cb662-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb662-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb662-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb662-119">-WhatIf</span></span>
<span data-ttu-id="cb662-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb662-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb662-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cb662-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb662-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb662-122">-DefaultProfile</span></span>
<span data-ttu-id="cb662-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb662-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb662-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb662-124">CommonParameters</span></span>
<span data-ttu-id="cb662-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb662-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb662-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb662-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb662-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb662-127">INPUTS</span></span>

### <span data-ttu-id="cb662-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cb662-128">PSWorkspace</span></span>
<span data-ttu-id="cb662-129">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="cb662-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="cb662-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb662-130">OUTPUTS</span></span>

### <span data-ttu-id="cb662-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="cb662-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="cb662-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb662-132">NOTES</span></span>
* <span data-ttu-id="cb662-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="cb662-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="cb662-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb662-134">RELATED LINKS</span></span>

[<span data-ttu-id="cb662-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="cb662-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


