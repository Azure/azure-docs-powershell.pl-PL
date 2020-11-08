---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224289"
---
# <span data-ttu-id="7d5ea-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="7d5ea-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="7d5ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d5ea-102">SYNOPSIS</span></span>
<span data-ttu-id="7d5ea-103">Usuwa klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="7d5ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d5ea-104">SYNTAX</span></span>

### <span data-ttu-id="7d5ea-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7d5ea-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d5ea-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7d5ea-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d5ea-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7d5ea-107">DESCRIPTION</span></span>
<span data-ttu-id="7d5ea-108">Usuwa klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="7d5ea-109">Jeśli istnieje wiele kluczy o tej samej nazwie, zostanie usunięta pierwsza z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="7d5ea-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d5ea-110">EXAMPLES</span></span>

### <span data-ttu-id="7d5ea-111">Przykład 1 Usuwanie IotHub</span><span class="sxs-lookup"><span data-stu-id="7d5ea-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="7d5ea-112">Usuwa klucz o nazwie iothubowner1 z IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="7d5ea-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7d5ea-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d5ea-113">PARAMETERS</span></span>

### <span data-ttu-id="7d5ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d5ea-114">-DefaultProfile</span></span>
<span data-ttu-id="7d5ea-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7d5ea-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d5ea-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="7d5ea-116">-HubId</span></span>
<span data-ttu-id="7d5ea-117">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="7d5ea-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5ea-118">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="7d5ea-118">-KeyName</span></span>
<span data-ttu-id="7d5ea-119">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="7d5ea-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5ea-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d5ea-120">-Name</span></span>
<span data-ttu-id="7d5ea-121">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="7d5ea-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d5ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d5ea-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7d5ea-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5ea-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d5ea-124">-Confirm</span></span>
<span data-ttu-id="7d5ea-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d5ea-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d5ea-126">-WhatIf</span></span>
<span data-ttu-id="7d5ea-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d5ea-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d5ea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d5ea-129">CommonParameters</span></span>
<span data-ttu-id="7d5ea-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d5ea-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d5ea-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d5ea-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d5ea-132">INPUTS</span></span>

### <span data-ttu-id="7d5ea-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7d5ea-133">System.String</span></span>

## <span data-ttu-id="7d5ea-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d5ea-134">OUTPUTS</span></span>

### <span data-ttu-id="7d5ea-135">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7d5ea-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="7d5ea-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d5ea-136">NOTES</span></span>

## <span data-ttu-id="7d5ea-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d5ea-137">RELATED LINKS</span></span>
