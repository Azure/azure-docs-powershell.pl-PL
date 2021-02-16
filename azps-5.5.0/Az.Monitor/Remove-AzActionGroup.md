---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: ebe0ecd51b59c6ff28fc0b5655a9b8ba6b8b4ee6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180115"
---
# <span data-ttu-id="38b94-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="38b94-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="38b94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38b94-102">SYNOPSIS</span></span>
<span data-ttu-id="38b94-103">Usuwa grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="38b94-103">Removes an action group.</span></span>

## <span data-ttu-id="38b94-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="38b94-104">SYNTAX</span></span>

### <span data-ttu-id="38b94-105">ByPropertyName (Default)</span><span class="sxs-lookup"><span data-stu-id="38b94-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b94-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="38b94-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38b94-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="38b94-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38b94-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="38b94-108">DESCRIPTION</span></span>
<span data-ttu-id="38b94-109">Polecenie **cmdlet Remove-AzActionGroup** usuwa grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="38b94-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="38b94-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="38b94-110">EXAMPLES</span></span>

### <span data-ttu-id="38b94-111">Przykład 1. Usuwanie grupy akcji</span><span class="sxs-lookup"><span data-stu-id="38b94-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="38b94-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38b94-112">PARAMETERS</span></span>

### <span data-ttu-id="38b94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b94-113">-DefaultProfile</span></span>
<span data-ttu-id="38b94-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="38b94-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38b94-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38b94-115">-InputObject</span></span>
<span data-ttu-id="38b94-116">Zasób grupy akcji</span><span class="sxs-lookup"><span data-stu-id="38b94-116">The action group resource</span></span>

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

### <span data-ttu-id="38b94-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="38b94-117">-Name</span></span>
<span data-ttu-id="38b94-118">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="38b94-118">The name of the action group.</span></span>

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

### <span data-ttu-id="38b94-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b94-119">-ResourceGroupName</span></span>
<span data-ttu-id="38b94-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="38b94-120">The resource group nam</span></span>

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

### <span data-ttu-id="38b94-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38b94-121">-ResourceId</span></span>
<span data-ttu-id="38b94-122">Zasób i</span><span class="sxs-lookup"><span data-stu-id="38b94-122">The resource i</span></span>

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

### <span data-ttu-id="38b94-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38b94-123">-Confirm</span></span>
<span data-ttu-id="38b94-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="38b94-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38b94-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b94-125">-WhatIf</span></span>
<span data-ttu-id="38b94-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38b94-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38b94-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="38b94-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38b94-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b94-128">CommonParameters</span></span>
<span data-ttu-id="38b94-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b94-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b94-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38b94-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b94-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38b94-131">INPUTS</span></span>

### <span data-ttu-id="38b94-132">System.String</span><span class="sxs-lookup"><span data-stu-id="38b94-132">System.String</span></span>

### <span data-ttu-id="38b94-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="38b94-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="38b94-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38b94-134">OUTPUTS</span></span>

### <span data-ttu-id="38b94-135">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="38b94-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="38b94-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="38b94-136">NOTES</span></span>

## <span data-ttu-id="38b94-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38b94-137">RELATED LINKS</span></span>

<span data-ttu-id="38b94-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="38b94-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
