---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 4f9412dd53c15b3c9b502d5cfde10eb4db7f3298
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718034"
---
# <span data-ttu-id="1c477-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="1c477-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="1c477-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c477-102">SYNOPSIS</span></span>
<span data-ttu-id="1c477-103">Zatrzymuje zbieranie danych dziennika systemu z komputerów Linux.</span><span class="sxs-lookup"><span data-stu-id="1c477-103">Stops collection of syslog data from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c477-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c477-104">SYNTAX</span></span>

### <span data-ttu-id="1c477-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c477-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c477-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1c477-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c477-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1c477-107">DESCRIPTION</span></span>
<span data-ttu-id="1c477-108">Polecenie cmdlet **disable-AzureRmOperationalInsightsLinuxSyslogCollection** zatrzymuje zbieranie danych dziennika systemu z połączonych komputerów Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="1c477-108">The **Disable-AzureRmOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="1c477-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c477-109">EXAMPLES</span></span>

## <span data-ttu-id="1c477-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c477-110">PARAMETERS</span></span>

### <span data-ttu-id="1c477-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c477-111">-DefaultProfile</span></span>
<span data-ttu-id="1c477-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1c477-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c477-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c477-113">-ResourceGroupName</span></span>
<span data-ttu-id="1c477-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="1c477-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="1c477-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="1c477-115">-Workspace</span></span>
<span data-ttu-id="1c477-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c477-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1c477-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="1c477-117">-WorkspaceName</span></span>
<span data-ttu-id="1c477-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c477-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1c477-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c477-119">-Confirm</span></span>
<span data-ttu-id="1c477-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c477-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c477-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c477-121">-WhatIf</span></span>
<span data-ttu-id="1c477-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c477-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c477-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c477-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c477-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c477-124">CommonParameters</span></span>
<span data-ttu-id="1c477-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c477-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c477-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c477-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c477-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c477-127">INPUTS</span></span>

### <span data-ttu-id="1c477-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1c477-128">PSWorkspace</span></span>
<span data-ttu-id="1c477-129">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="1c477-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="1c477-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c477-130">OUTPUTS</span></span>

### <span data-ttu-id="1c477-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1c477-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1c477-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c477-132">NOTES</span></span>
* <span data-ttu-id="1c477-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="1c477-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="1c477-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c477-134">RELATED LINKS</span></span>

[<span data-ttu-id="1c477-135">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="1c477-135">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="1c477-136">Nowe — AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="1c477-136">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


