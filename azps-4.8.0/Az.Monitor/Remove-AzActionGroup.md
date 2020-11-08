---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: ebe0ecd51b59c6ff28fc0b5655a9b8ba6b8b4ee6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220761"
---
# <span data-ttu-id="92efc-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="92efc-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="92efc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92efc-102">SYNOPSIS</span></span>
<span data-ttu-id="92efc-103">Usuwa grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="92efc-103">Removes an action group.</span></span>

## <span data-ttu-id="92efc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92efc-104">SYNTAX</span></span>

### <span data-ttu-id="92efc-105">ByPropertyName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="92efc-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92efc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="92efc-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92efc-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92efc-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92efc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="92efc-108">DESCRIPTION</span></span>
<span data-ttu-id="92efc-109">Polecenie cmdlet **Remove-AzActionGroup** usuwa grupę Actions.</span><span class="sxs-lookup"><span data-stu-id="92efc-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="92efc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92efc-110">EXAMPLES</span></span>

### <span data-ttu-id="92efc-111">Przykład 1. Usuń grupę akcji</span><span class="sxs-lookup"><span data-stu-id="92efc-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="92efc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92efc-112">PARAMETERS</span></span>

### <span data-ttu-id="92efc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92efc-113">-DefaultProfile</span></span>
<span data-ttu-id="92efc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="92efc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92efc-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="92efc-115">-InputObject</span></span>
<span data-ttu-id="92efc-116">Zasób grupa akcji</span><span class="sxs-lookup"><span data-stu-id="92efc-116">The action group resource</span></span>

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

### <span data-ttu-id="92efc-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92efc-117">-Name</span></span>
<span data-ttu-id="92efc-118">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="92efc-118">The name of the action group.</span></span>

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

### <span data-ttu-id="92efc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92efc-119">-ResourceGroupName</span></span>
<span data-ttu-id="92efc-120">Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="92efc-120">The resource group nam</span></span>

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

### <span data-ttu-id="92efc-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92efc-121">-ResourceId</span></span>
<span data-ttu-id="92efc-122">Zasób i</span><span class="sxs-lookup"><span data-stu-id="92efc-122">The resource i</span></span>

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

### <span data-ttu-id="92efc-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92efc-123">-Confirm</span></span>
<span data-ttu-id="92efc-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92efc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92efc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92efc-125">-WhatIf</span></span>
<span data-ttu-id="92efc-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92efc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92efc-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92efc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92efc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92efc-128">CommonParameters</span></span>
<span data-ttu-id="92efc-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92efc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92efc-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92efc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92efc-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92efc-131">INPUTS</span></span>

### <span data-ttu-id="92efc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="92efc-132">System.String</span></span>

### <span data-ttu-id="92efc-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="92efc-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="92efc-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92efc-134">OUTPUTS</span></span>

### <span data-ttu-id="92efc-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="92efc-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="92efc-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92efc-136">NOTES</span></span>

## <span data-ttu-id="92efc-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92efc-137">RELATED LINKS</span></span>

<span data-ttu-id="92efc-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Nowe — AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="92efc-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
