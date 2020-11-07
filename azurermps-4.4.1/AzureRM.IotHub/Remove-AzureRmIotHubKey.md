---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 8b7603f145d45411b20b124823f28281d4117127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716690"
---
# <span data-ttu-id="44151-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="44151-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="44151-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44151-102">SYNOPSIS</span></span>
<span data-ttu-id="44151-103">Usuwa klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="44151-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44151-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44151-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44151-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44151-105">DESCRIPTION</span></span>
<span data-ttu-id="44151-106">Usuwa klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="44151-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="44151-107">Jeśli istnieje wiele kluczy o tej samej nazwie, zostanie usunięta pierwsza z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="44151-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="44151-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44151-108">EXAMPLES</span></span>

### <span data-ttu-id="44151-109">Przykład 1 Usuwanie IotHub</span><span class="sxs-lookup"><span data-stu-id="44151-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="44151-110">Usuwa klucz o nazwie iothubowner1 z IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="44151-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="44151-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44151-111">PARAMETERS</span></span>

### <span data-ttu-id="44151-112">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="44151-112">-KeyName</span></span>
<span data-ttu-id="44151-113">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="44151-113">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44151-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44151-114">-Name</span></span>
<span data-ttu-id="44151-115">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="44151-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="44151-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44151-116">-ResourceGroupName</span></span>
<span data-ttu-id="44151-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="44151-117">Resource Group Name</span></span>

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

### <span data-ttu-id="44151-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44151-118">-Confirm</span></span>
<span data-ttu-id="44151-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44151-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44151-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44151-120">-WhatIf</span></span>
<span data-ttu-id="44151-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44151-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44151-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="44151-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44151-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44151-123">-DefaultProfile</span></span>
<span data-ttu-id="44151-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44151-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44151-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44151-125">CommonParameters</span></span>
<span data-ttu-id="44151-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44151-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44151-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44151-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44151-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44151-128">INPUTS</span></span>

### <span data-ttu-id="44151-129">System. String</span><span class="sxs-lookup"><span data-stu-id="44151-129">System.String</span></span>

## <span data-ttu-id="44151-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44151-130">OUTPUTS</span></span>

### <span data-ttu-id="44151-131">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. IotHub. platforms. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="44151-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="44151-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44151-132">NOTES</span></span>

## <span data-ttu-id="44151-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44151-133">RELATED LINKS</span></span>

