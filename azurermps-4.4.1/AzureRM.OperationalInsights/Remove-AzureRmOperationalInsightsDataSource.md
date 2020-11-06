---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 49674f372e477ee7050a6ccf7d833aaee59bac3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543111"
---
# <span data-ttu-id="9c010-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9c010-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="9c010-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c010-102">SYNOPSIS</span></span>
<span data-ttu-id="9c010-103">Usuwa źródło danych.</span><span class="sxs-lookup"><span data-stu-id="9c010-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c010-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c010-104">SYNTAX</span></span>

### <span data-ttu-id="9c010-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9c010-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c010-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9c010-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c010-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9c010-107">DESCRIPTION</span></span>
<span data-ttu-id="9c010-108">Polecenie cmdlet **Remove-AzureRmOperationalInsightsDataSource** usuwa źródło danych.</span><span class="sxs-lookup"><span data-stu-id="9c010-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="9c010-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c010-109">EXAMPLES</span></span>

## <span data-ttu-id="9c010-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c010-110">PARAMETERS</span></span>

### <span data-ttu-id="9c010-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9c010-111">-Force</span></span>
<span data-ttu-id="9c010-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9c010-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c010-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9c010-113">-Name</span></span>
<span data-ttu-id="9c010-114">Określa nazwę źródła danych, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="9c010-114">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c010-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c010-115">-ResourceGroupName</span></span>
<span data-ttu-id="9c010-116">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="9c010-116">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="9c010-117">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="9c010-117">-Workspace</span></span>
<span data-ttu-id="9c010-118">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c010-118">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9c010-119">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="9c010-119">-WorkspaceName</span></span>
<span data-ttu-id="9c010-120">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c010-120">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9c010-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c010-121">-Confirm</span></span>
<span data-ttu-id="9c010-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c010-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c010-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c010-123">-WhatIf</span></span>
<span data-ttu-id="9c010-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c010-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c010-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9c010-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c010-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c010-126">-DefaultProfile</span></span>
<span data-ttu-id="9c010-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c010-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c010-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c010-128">CommonParameters</span></span>
<span data-ttu-id="9c010-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c010-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c010-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c010-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c010-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c010-131">INPUTS</span></span>

### <span data-ttu-id="9c010-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9c010-132">PSWorkspace</span></span>
<span data-ttu-id="9c010-133">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="9c010-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="9c010-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c010-134">OUTPUTS</span></span>

## <span data-ttu-id="9c010-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c010-135">NOTES</span></span>
* <span data-ttu-id="9c010-136">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="9c010-136">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="9c010-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c010-137">RELATED LINKS</span></span>

[<span data-ttu-id="9c010-138">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9c010-138">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="9c010-139">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9c010-139">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


