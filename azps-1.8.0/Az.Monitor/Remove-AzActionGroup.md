---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: dc32d17a887c4a8c9cfd15f952c1d411a8ef1700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709770"
---
# <span data-ttu-id="a3325-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="a3325-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="a3325-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3325-102">SYNOPSIS</span></span>
<span data-ttu-id="a3325-103">Usuwa grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="a3325-103">Removes an action group.</span></span>

## <span data-ttu-id="a3325-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3325-104">SYNTAX</span></span>

### <span data-ttu-id="a3325-105">ByPropertyName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a3325-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3325-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a3325-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3325-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a3325-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3325-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a3325-108">DESCRIPTION</span></span>
<span data-ttu-id="a3325-109">Polecenie cmdlet **Remove-AzActionGroup** usuwa grupę Actions.</span><span class="sxs-lookup"><span data-stu-id="a3325-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="a3325-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3325-110">EXAMPLES</span></span>

### <span data-ttu-id="a3325-111">Przykład 1. Usuń grupę akcji</span><span class="sxs-lookup"><span data-stu-id="a3325-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="a3325-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3325-112">PARAMETERS</span></span>

### <span data-ttu-id="a3325-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3325-113">-DefaultProfile</span></span>
<span data-ttu-id="a3325-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a3325-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3325-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a3325-115">-InputObject</span></span>
<span data-ttu-id="a3325-116">Grupa akcji resourc</span><span class="sxs-lookup"><span data-stu-id="a3325-116">The action group resourc</span></span>

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

### <span data-ttu-id="a3325-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3325-117">-Name</span></span>
<span data-ttu-id="a3325-118">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="a3325-118">The name of the action group.</span></span>

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

### <span data-ttu-id="a3325-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3325-119">-ResourceGroupName</span></span>
<span data-ttu-id="a3325-120">Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="a3325-120">The resource group nam</span></span>

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

### <span data-ttu-id="a3325-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3325-121">-ResourceId</span></span>
<span data-ttu-id="a3325-122">Zasób i</span><span class="sxs-lookup"><span data-stu-id="a3325-122">The resource i</span></span>

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

### <span data-ttu-id="a3325-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3325-123">-Confirm</span></span>
<span data-ttu-id="a3325-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3325-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3325-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3325-125">-WhatIf</span></span>
<span data-ttu-id="a3325-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3325-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3325-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3325-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3325-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3325-128">CommonParameters</span></span>
<span data-ttu-id="a3325-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3325-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3325-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3325-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3325-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3325-131">INPUTS</span></span>

### <span data-ttu-id="a3325-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a3325-132">System.String</span></span>

### <span data-ttu-id="a3325-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="a3325-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="a3325-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3325-134">OUTPUTS</span></span>

### <span data-ttu-id="a3325-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a3325-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="a3325-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3325-136">NOTES</span></span>

## <span data-ttu-id="a3325-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3325-137">RELATED LINKS</span></span>

<span data-ttu-id="a3325-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Nowe — AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="a3325-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
