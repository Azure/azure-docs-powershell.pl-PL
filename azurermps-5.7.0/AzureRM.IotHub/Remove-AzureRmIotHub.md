---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 1da7b9981b3c2fe96d895290b7ab73dfc36e183e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545671"
---
# <span data-ttu-id="7461e-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="7461e-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="7461e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7461e-102">SYNOPSIS</span></span>
<span data-ttu-id="7461e-103">Usuwa IotHub.</span><span class="sxs-lookup"><span data-stu-id="7461e-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7461e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7461e-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7461e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7461e-105">DESCRIPTION</span></span>
<span data-ttu-id="7461e-106">Usuwa IotHub.</span><span class="sxs-lookup"><span data-stu-id="7461e-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="7461e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7461e-107">EXAMPLES</span></span>

### <span data-ttu-id="7461e-108">Przykład 1 Usuwanie IotHub</span><span class="sxs-lookup"><span data-stu-id="7461e-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7461e-109">Usuwa IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="7461e-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="7461e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7461e-110">PARAMETERS</span></span>

### <span data-ttu-id="7461e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7461e-111">-DefaultProfile</span></span>
<span data-ttu-id="7461e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7461e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7461e-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7461e-113">-Name</span></span>
<span data-ttu-id="7461e-114">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="7461e-114">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7461e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7461e-115">-ResourceGroupName</span></span>
<span data-ttu-id="7461e-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7461e-116">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7461e-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7461e-117">-Confirm</span></span>
<span data-ttu-id="7461e-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7461e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7461e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7461e-119">-WhatIf</span></span>
<span data-ttu-id="7461e-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7461e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7461e-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7461e-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7461e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7461e-122">CommonParameters</span></span>
<span data-ttu-id="7461e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7461e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7461e-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7461e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7461e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7461e-125">INPUTS</span></span>

### <span data-ttu-id="7461e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7461e-126">System.String</span></span>

## <span data-ttu-id="7461e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7461e-127">OUTPUTS</span></span>

### <span data-ttu-id="7461e-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="7461e-128">System.Object</span></span>

## <span data-ttu-id="7461e-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7461e-129">NOTES</span></span>

## <span data-ttu-id="7461e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7461e-130">RELATED LINKS</span></span>
