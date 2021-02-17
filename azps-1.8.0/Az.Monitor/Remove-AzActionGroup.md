---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: b1c77b2a00f460e6d05483037a46e5472a25d266
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403038"
---
# <span data-ttu-id="145ed-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="145ed-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="145ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="145ed-102">SYNOPSIS</span></span>
<span data-ttu-id="145ed-103">Usuwa grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="145ed-103">Removes an action group.</span></span>

## <span data-ttu-id="145ed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="145ed-104">SYNTAX</span></span>

### <span data-ttu-id="145ed-105">ByPropertyName (Default)</span><span class="sxs-lookup"><span data-stu-id="145ed-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="145ed-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="145ed-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="145ed-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="145ed-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="145ed-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="145ed-108">DESCRIPTION</span></span>
<span data-ttu-id="145ed-109">Polecenie **cmdlet Remove-AzActionGroup** usuwa grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="145ed-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="145ed-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="145ed-110">EXAMPLES</span></span>

### <span data-ttu-id="145ed-111">Przykład 1. Usuwanie grupy akcji</span><span class="sxs-lookup"><span data-stu-id="145ed-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="145ed-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="145ed-112">PARAMETERS</span></span>

### <span data-ttu-id="145ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145ed-113">-DefaultProfile</span></span>
<span data-ttu-id="145ed-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="145ed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="145ed-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="145ed-115">-InputObject</span></span>
<span data-ttu-id="145ed-116">Zasobów grupy akcji</span><span class="sxs-lookup"><span data-stu-id="145ed-116">The action group resourc</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="145ed-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="145ed-117">-Name</span></span>
<span data-ttu-id="145ed-118">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="145ed-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="145ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="145ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="145ed-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="145ed-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="145ed-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="145ed-121">-ResourceId</span></span>
<span data-ttu-id="145ed-122">Zasób i</span><span class="sxs-lookup"><span data-stu-id="145ed-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="145ed-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="145ed-123">-Confirm</span></span>
<span data-ttu-id="145ed-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="145ed-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="145ed-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="145ed-125">-WhatIf</span></span>
<span data-ttu-id="145ed-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="145ed-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="145ed-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="145ed-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="145ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145ed-128">CommonParameters</span></span>
<span data-ttu-id="145ed-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="145ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145ed-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="145ed-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145ed-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="145ed-131">INPUTS</span></span>

### <span data-ttu-id="145ed-132">System.String</span><span class="sxs-lookup"><span data-stu-id="145ed-132">System.String</span></span>

### <span data-ttu-id="145ed-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="145ed-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="145ed-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="145ed-134">OUTPUTS</span></span>

### <span data-ttu-id="145ed-135">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="145ed-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="145ed-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="145ed-136">NOTES</span></span>

## <span data-ttu-id="145ed-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="145ed-137">RELATED LINKS</span></span>

<span data-ttu-id="145ed-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="145ed-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)</span></span>

