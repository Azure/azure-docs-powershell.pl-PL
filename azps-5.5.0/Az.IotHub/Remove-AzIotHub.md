---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200090"
---
# <span data-ttu-id="7a844-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="7a844-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="7a844-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a844-102">SYNOPSIS</span></span>
<span data-ttu-id="7a844-103">Usuwa element iotHub.</span><span class="sxs-lookup"><span data-stu-id="7a844-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="7a844-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7a844-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a844-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7a844-105">DESCRIPTION</span></span>
<span data-ttu-id="7a844-106">Usuwa element iotHub.</span><span class="sxs-lookup"><span data-stu-id="7a844-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="7a844-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7a844-107">EXAMPLES</span></span>

### <span data-ttu-id="7a844-108">Przykład 1. Usuwanie aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="7a844-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7a844-109">Usuwa element iotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="7a844-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="7a844-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a844-110">PARAMETERS</span></span>

### <span data-ttu-id="7a844-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a844-111">-DefaultProfile</span></span>
<span data-ttu-id="7a844-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7a844-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a844-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7a844-113">-Name</span></span>
<span data-ttu-id="7a844-114">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="7a844-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="7a844-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a844-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a844-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7a844-116">Resource Group Name</span></span>

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

### <span data-ttu-id="7a844-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a844-117">-Confirm</span></span>
<span data-ttu-id="7a844-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7a844-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a844-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a844-119">-WhatIf</span></span>
<span data-ttu-id="7a844-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a844-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a844-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7a844-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a844-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a844-122">CommonParameters</span></span>
<span data-ttu-id="7a844-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a844-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a844-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a844-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a844-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a844-125">INPUTS</span></span>

### <span data-ttu-id="7a844-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7a844-126">System.String</span></span>

## <span data-ttu-id="7a844-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a844-127">OUTPUTS</span></span>

### <span data-ttu-id="7a844-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="7a844-128">System.Void</span></span>

## <span data-ttu-id="7a844-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7a844-129">NOTES</span></span>

## <span data-ttu-id="7a844-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a844-130">RELATED LINKS</span></span>
