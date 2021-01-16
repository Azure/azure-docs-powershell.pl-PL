---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337045"
---
# <span data-ttu-id="a3b09-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="a3b09-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="a3b09-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3b09-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b09-103">Usuwa IotHub.</span><span class="sxs-lookup"><span data-stu-id="a3b09-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="a3b09-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3b09-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3b09-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3b09-105">DESCRIPTION</span></span>
<span data-ttu-id="a3b09-106">Usuwa IotHub.</span><span class="sxs-lookup"><span data-stu-id="a3b09-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="a3b09-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3b09-107">EXAMPLES</span></span>

### <span data-ttu-id="a3b09-108">Przykład 1 Usuwanie IotHub</span><span class="sxs-lookup"><span data-stu-id="a3b09-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a3b09-109">Usuwa IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a3b09-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="a3b09-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3b09-110">PARAMETERS</span></span>

### <span data-ttu-id="a3b09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b09-111">-DefaultProfile</span></span>
<span data-ttu-id="a3b09-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a3b09-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3b09-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3b09-113">-Name</span></span>
<span data-ttu-id="a3b09-114">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="a3b09-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="a3b09-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b09-115">-ResourceGroupName</span></span>
<span data-ttu-id="a3b09-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a3b09-116">Resource Group Name</span></span>

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

### <span data-ttu-id="a3b09-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3b09-117">-Confirm</span></span>
<span data-ttu-id="a3b09-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3b09-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3b09-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3b09-119">-WhatIf</span></span>
<span data-ttu-id="a3b09-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3b09-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3b09-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3b09-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3b09-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b09-122">CommonParameters</span></span>
<span data-ttu-id="a3b09-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3b09-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b09-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3b09-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b09-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3b09-125">INPUTS</span></span>

### <span data-ttu-id="a3b09-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a3b09-126">System.String</span></span>

## <span data-ttu-id="a3b09-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3b09-127">OUTPUTS</span></span>

### <span data-ttu-id="a3b09-128">System. void</span><span class="sxs-lookup"><span data-stu-id="a3b09-128">System.Void</span></span>

## <span data-ttu-id="a3b09-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3b09-129">NOTES</span></span>

## <span data-ttu-id="a3b09-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3b09-130">RELATED LINKS</span></span>
