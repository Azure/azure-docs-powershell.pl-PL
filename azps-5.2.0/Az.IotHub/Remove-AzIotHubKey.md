---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330865"
---
# <span data-ttu-id="ec294-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="ec294-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="ec294-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec294-102">SYNOPSIS</span></span>
<span data-ttu-id="ec294-103">Usuwa klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="ec294-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="ec294-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec294-104">SYNTAX</span></span>

### <span data-ttu-id="ec294-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ec294-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec294-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ec294-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec294-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ec294-107">DESCRIPTION</span></span>
<span data-ttu-id="ec294-108">Usuwa klucz IotHub.</span><span class="sxs-lookup"><span data-stu-id="ec294-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="ec294-109">Jeśli istnieje wiele kluczy o tej samej nazwie, zostanie usunięta pierwsza z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="ec294-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="ec294-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec294-110">EXAMPLES</span></span>

### <span data-ttu-id="ec294-111">Przykład 1 Usuwanie IotHub</span><span class="sxs-lookup"><span data-stu-id="ec294-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="ec294-112">Usuwa klucz o nazwie iothubowner1 z IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="ec294-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ec294-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec294-113">PARAMETERS</span></span>

### <span data-ttu-id="ec294-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec294-114">-DefaultProfile</span></span>
<span data-ttu-id="ec294-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ec294-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec294-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="ec294-116">-HubId</span></span>
<span data-ttu-id="ec294-117">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="ec294-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ec294-118">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="ec294-118">-KeyName</span></span>
<span data-ttu-id="ec294-119">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="ec294-119">Name of the Key</span></span>

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

### <span data-ttu-id="ec294-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec294-120">-Name</span></span>
<span data-ttu-id="ec294-121">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="ec294-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="ec294-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec294-122">-ResourceGroupName</span></span>
<span data-ttu-id="ec294-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ec294-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ec294-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec294-124">-Confirm</span></span>
<span data-ttu-id="ec294-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec294-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec294-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec294-126">-WhatIf</span></span>
<span data-ttu-id="ec294-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec294-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec294-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ec294-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec294-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec294-129">CommonParameters</span></span>
<span data-ttu-id="ec294-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec294-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec294-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec294-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec294-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec294-132">INPUTS</span></span>

### <span data-ttu-id="ec294-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ec294-133">System.String</span></span>

## <span data-ttu-id="ec294-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec294-134">OUTPUTS</span></span>

### <span data-ttu-id="ec294-135">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ec294-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="ec294-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec294-136">NOTES</span></span>

## <span data-ttu-id="ec294-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec294-137">RELATED LINKS</span></span>
