---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327796"
---
# <span data-ttu-id="89dc2-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="89dc2-101">Update-AzAlertState</span></span>

## <span data-ttu-id="89dc2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="89dc2-103">Stan alertu aktualizacji</span><span class="sxs-lookup"><span data-stu-id="89dc2-103">Updates alert state</span></span>

## <span data-ttu-id="89dc2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89dc2-104">SYNTAX</span></span>

### <span data-ttu-id="89dc2-105">ByAlertId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="89dc2-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89dc2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="89dc2-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89dc2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="89dc2-107">DESCRIPTION</span></span>
<span data-ttu-id="89dc2-108">Polecenie cmdlet **Update-AzAlertState** umożliwia aktualizowanie stanu alertu.</span><span class="sxs-lookup"><span data-stu-id="89dc2-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="89dc2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89dc2-109">EXAMPLES</span></span>

### <span data-ttu-id="89dc2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="89dc2-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="89dc2-111">To polecenie cmdlet umożliwia zaktualizowanie stanu alertu na zamknięty.</span><span class="sxs-lookup"><span data-stu-id="89dc2-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="89dc2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89dc2-112">PARAMETERS</span></span>

### <span data-ttu-id="89dc2-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="89dc2-113">-AlertId</span></span>
<span data-ttu-id="89dc2-114">Unikatowy identyfikator alertu/ResourceId alertu.</span><span class="sxs-lookup"><span data-stu-id="89dc2-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89dc2-115">-DefaultProfile</span></span>
<span data-ttu-id="89dc2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89dc2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dc2-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="89dc2-117">-InputObject</span></span>
<span data-ttu-id="89dc2-118">Obiekt wejściowy z potoku.</span><span class="sxs-lookup"><span data-stu-id="89dc2-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89dc2-119">-State</span><span class="sxs-lookup"><span data-stu-id="89dc2-119">-State</span></span>
<span data-ttu-id="89dc2-120">Zaktualizowany stan alertu</span><span class="sxs-lookup"><span data-stu-id="89dc2-120">Updated Alert State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dc2-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89dc2-121">-Confirm</span></span>
<span data-ttu-id="89dc2-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89dc2-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dc2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89dc2-123">-WhatIf</span></span>
<span data-ttu-id="89dc2-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89dc2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89dc2-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89dc2-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dc2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89dc2-126">CommonParameters</span></span>
<span data-ttu-id="89dc2-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89dc2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89dc2-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89dc2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89dc2-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89dc2-129">INPUTS</span></span>

### <span data-ttu-id="89dc2-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="89dc2-130">None</span></span>

## <span data-ttu-id="89dc2-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89dc2-131">OUTPUTS</span></span>

### <span data-ttu-id="89dc2-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="89dc2-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="89dc2-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89dc2-133">NOTES</span></span>

## <span data-ttu-id="89dc2-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89dc2-134">RELATED LINKS</span></span>
