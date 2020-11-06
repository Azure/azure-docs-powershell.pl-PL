---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 0f3a6bfa99a199a737c7a69d151d29f5918cc502
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550979"
---
# <span data-ttu-id="ba0a4-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="ba0a4-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="ba0a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba0a4-103">Usuwa IotHub.</span><span class="sxs-lookup"><span data-stu-id="ba0a4-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba0a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba0a4-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba0a4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba0a4-105">DESCRIPTION</span></span>
<span data-ttu-id="ba0a4-106">Usuwa IotHub.</span><span class="sxs-lookup"><span data-stu-id="ba0a4-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="ba0a4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba0a4-107">EXAMPLES</span></span>

### <span data-ttu-id="ba0a4-108">Przykład 1 Usuwanie IotHub</span><span class="sxs-lookup"><span data-stu-id="ba0a4-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ba0a4-109">Usuwa IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="ba0a4-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="ba0a4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba0a4-110">PARAMETERS</span></span>

### <span data-ttu-id="ba0a4-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ba0a4-111">-Name</span></span>
<span data-ttu-id="ba0a4-112">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="ba0a4-112">Name of the IotHub</span></span>

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

### <span data-ttu-id="ba0a4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba0a4-113">-ResourceGroupName</span></span>
<span data-ttu-id="ba0a4-114">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ba0a4-114">Resource Group Name</span></span>

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

### <span data-ttu-id="ba0a4-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba0a4-115">-Confirm</span></span>
<span data-ttu-id="ba0a4-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba0a4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba0a4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba0a4-117">-WhatIf</span></span>
<span data-ttu-id="ba0a4-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba0a4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba0a4-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ba0a4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba0a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba0a4-120">-DefaultProfile</span></span>
<span data-ttu-id="ba0a4-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba0a4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba0a4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba0a4-122">CommonParameters</span></span>
<span data-ttu-id="ba0a4-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba0a4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba0a4-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba0a4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba0a4-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba0a4-125">INPUTS</span></span>

### <span data-ttu-id="ba0a4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ba0a4-126">System.String</span></span>

## <span data-ttu-id="ba0a4-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba0a4-127">OUTPUTS</span></span>

### <span data-ttu-id="ba0a4-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="ba0a4-128">System.Object</span></span>

## <span data-ttu-id="ba0a4-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba0a4-129">NOTES</span></span>

## <span data-ttu-id="ba0a4-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba0a4-130">RELATED LINKS</span></span>

