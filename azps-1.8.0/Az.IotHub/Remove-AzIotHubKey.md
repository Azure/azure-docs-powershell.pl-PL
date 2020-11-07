---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c275ac087c24c58de73e72ac5dcf46839d710621
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868071"
---
# <span data-ttu-id="aa27a-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="aa27a-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="aa27a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa27a-102">SYNOPSIS</span></span>
<span data-ttu-id="aa27a-103">Usuwa klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="aa27a-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="aa27a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa27a-104">SYNTAX</span></span>

```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa27a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa27a-105">DESCRIPTION</span></span>
<span data-ttu-id="aa27a-106">Usuwa klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="aa27a-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="aa27a-107">Jeśli istnieje wiele kluczy o tej samej nazwie, zostanie usunięta pierwsza z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="aa27a-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="aa27a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa27a-108">EXAMPLES</span></span>

### <span data-ttu-id="aa27a-109">Przykład 1 Usuwanie IotHub</span><span class="sxs-lookup"><span data-stu-id="aa27a-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="aa27a-110">Usuwa klucz o nazwie iothubowner1 z IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="aa27a-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="aa27a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa27a-111">PARAMETERS</span></span>

### <span data-ttu-id="aa27a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa27a-112">-DefaultProfile</span></span>
<span data-ttu-id="aa27a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="aa27a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa27a-114">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="aa27a-114">-KeyName</span></span>
<span data-ttu-id="aa27a-115">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="aa27a-115">Name of the Key</span></span>

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

### <span data-ttu-id="aa27a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa27a-116">-Name</span></span>
<span data-ttu-id="aa27a-117">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="aa27a-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="aa27a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa27a-118">-ResourceGroupName</span></span>
<span data-ttu-id="aa27a-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aa27a-119">Resource Group Name</span></span>

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

### <span data-ttu-id="aa27a-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa27a-120">-Confirm</span></span>
<span data-ttu-id="aa27a-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa27a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa27a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa27a-122">-WhatIf</span></span>
<span data-ttu-id="aa27a-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa27a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa27a-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa27a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa27a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa27a-125">CommonParameters</span></span>
<span data-ttu-id="aa27a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa27a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa27a-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa27a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa27a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa27a-128">INPUTS</span></span>

### <span data-ttu-id="aa27a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aa27a-129">System.String</span></span>

## <span data-ttu-id="aa27a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa27a-130">OUTPUTS</span></span>

### <span data-ttu-id="aa27a-131">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="aa27a-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="aa27a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa27a-132">NOTES</span></span>

## <span data-ttu-id="aa27a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa27a-133">RELATED LINKS</span></span>
