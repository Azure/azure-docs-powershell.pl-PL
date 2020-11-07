---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 0b5f84a38fcd087b77b32624b9cbd9b3b8a27e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719027"
---
# <span data-ttu-id="42831-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="42831-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="42831-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42831-102">SYNOPSIS</span></span>
<span data-ttu-id="42831-103">Usuwa grupę akcji.</span><span class="sxs-lookup"><span data-stu-id="42831-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42831-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42831-104">SYNTAX</span></span>

### <span data-ttu-id="42831-105">ByPropertyName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="42831-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42831-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="42831-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42831-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="42831-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42831-108">Opis</span><span class="sxs-lookup"><span data-stu-id="42831-108">DESCRIPTION</span></span>
<span data-ttu-id="42831-109">Polecenie cmdlet **Remove-AzureRmActionGroup** usuwa grupę Actions.</span><span class="sxs-lookup"><span data-stu-id="42831-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="42831-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42831-110">EXAMPLES</span></span>

### <span data-ttu-id="42831-111">Przykład 1. Usuń grupę akcji</span><span class="sxs-lookup"><span data-stu-id="42831-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="42831-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42831-112">PARAMETERS</span></span>

### <span data-ttu-id="42831-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42831-113">-Name</span></span>
<span data-ttu-id="42831-114">Nazwa grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="42831-114">The name of the action group.</span></span>

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

### <span data-ttu-id="42831-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42831-115">-Confirm</span></span>
<span data-ttu-id="42831-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42831-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42831-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42831-117">-DefaultProfile</span></span>
<span data-ttu-id="42831-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42831-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42831-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42831-119">-InputObject</span></span>
<span data-ttu-id="42831-120">Zasób grupa akcji</span><span class="sxs-lookup"><span data-stu-id="42831-120">The action group resource</span></span>

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

### <span data-ttu-id="42831-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42831-121">-ResourceGroupName</span></span>
<span data-ttu-id="42831-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="42831-122">The resource group name</span></span>

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

### <span data-ttu-id="42831-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42831-123">-ResourceId</span></span>
<span data-ttu-id="42831-124">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="42831-124">The resource id</span></span>

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

### <span data-ttu-id="42831-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42831-125">-WhatIf</span></span>
<span data-ttu-id="42831-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42831-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42831-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42831-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42831-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42831-128">CommonParameters</span></span>
<span data-ttu-id="42831-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42831-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42831-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42831-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42831-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42831-131">INPUTS</span></span>

## <span data-ttu-id="42831-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42831-132">OUTPUTS</span></span>

### <span data-ttu-id="42831-133">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="42831-133">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="42831-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42831-134">NOTES</span></span>

## <span data-ttu-id="42831-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42831-135">RELATED LINKS</span></span>

<span data-ttu-id="42831-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Nowe — AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="42831-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
