---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 0e83ec5266bc807f64bd231a3a423ad8cc7db190
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893081"
---
# <span data-ttu-id="55074-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="55074-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="55074-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55074-102">SYNOPSIS</span></span>
<span data-ttu-id="55074-103">Usuwa IotHub.</span><span class="sxs-lookup"><span data-stu-id="55074-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="55074-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55074-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55074-105">Opis</span><span class="sxs-lookup"><span data-stu-id="55074-105">DESCRIPTION</span></span>
<span data-ttu-id="55074-106">Usuwa IotHub.</span><span class="sxs-lookup"><span data-stu-id="55074-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="55074-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55074-107">EXAMPLES</span></span>

### <span data-ttu-id="55074-108">Przykład 1 Usuwanie IotHub</span><span class="sxs-lookup"><span data-stu-id="55074-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="55074-109">Usuwa IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="55074-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="55074-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55074-110">PARAMETERS</span></span>

### <span data-ttu-id="55074-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55074-111">-DefaultProfile</span></span>
<span data-ttu-id="55074-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="55074-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55074-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="55074-113">-Name</span></span>
<span data-ttu-id="55074-114">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="55074-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="55074-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55074-115">-ResourceGroupName</span></span>
<span data-ttu-id="55074-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="55074-116">Resource Group Name</span></span>

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

### <span data-ttu-id="55074-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55074-117">-Confirm</span></span>
<span data-ttu-id="55074-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55074-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55074-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55074-119">-WhatIf</span></span>
<span data-ttu-id="55074-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55074-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55074-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="55074-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55074-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55074-122">CommonParameters</span></span>
<span data-ttu-id="55074-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55074-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55074-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55074-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55074-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55074-125">INPUTS</span></span>

### <span data-ttu-id="55074-126">System. String</span><span class="sxs-lookup"><span data-stu-id="55074-126">System.String</span></span>

## <span data-ttu-id="55074-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55074-127">OUTPUTS</span></span>

### <span data-ttu-id="55074-128">System. void</span><span class="sxs-lookup"><span data-stu-id="55074-128">System.Void</span></span>

## <span data-ttu-id="55074-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55074-129">NOTES</span></span>

## <span data-ttu-id="55074-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55074-130">RELATED LINKS</span></span>
