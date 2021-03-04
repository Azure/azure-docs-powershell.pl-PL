---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 78478b28e42302ad3a672a0ee889f03807f3d1ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986035"
---
# <span data-ttu-id="be59b-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="be59b-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="be59b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be59b-102">SYNOPSIS</span></span>
<span data-ttu-id="be59b-103">Usuwa element iotHub.</span><span class="sxs-lookup"><span data-stu-id="be59b-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="be59b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be59b-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be59b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="be59b-105">DESCRIPTION</span></span>
<span data-ttu-id="be59b-106">Usuwa element iotHub.</span><span class="sxs-lookup"><span data-stu-id="be59b-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="be59b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be59b-107">EXAMPLES</span></span>

### <span data-ttu-id="be59b-108">Przykład 1. Usuwanie aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="be59b-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="be59b-109">Usuwa element iotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="be59b-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="be59b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be59b-110">PARAMETERS</span></span>

### <span data-ttu-id="be59b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be59b-111">-DefaultProfile</span></span>
<span data-ttu-id="be59b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="be59b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be59b-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="be59b-113">-Name</span></span>
<span data-ttu-id="be59b-114">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="be59b-114">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be59b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be59b-115">-ResourceGroupName</span></span>
<span data-ttu-id="be59b-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="be59b-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be59b-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be59b-117">-Confirm</span></span>
<span data-ttu-id="be59b-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="be59b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be59b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be59b-119">-WhatIf</span></span>
<span data-ttu-id="be59b-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be59b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be59b-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="be59b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be59b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be59b-122">CommonParameters</span></span>
<span data-ttu-id="be59b-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be59b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be59b-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be59b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be59b-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be59b-125">INPUTS</span></span>

### <span data-ttu-id="be59b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="be59b-126">System.String</span></span>

## <span data-ttu-id="be59b-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be59b-127">OUTPUTS</span></span>

### <span data-ttu-id="be59b-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="be59b-128">System.Void</span></span>

## <span data-ttu-id="be59b-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be59b-129">NOTES</span></span>

## <span data-ttu-id="be59b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be59b-130">RELATED LINKS</span></span>
