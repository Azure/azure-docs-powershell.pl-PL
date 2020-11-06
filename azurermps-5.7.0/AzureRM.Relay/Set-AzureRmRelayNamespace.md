---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 09c601e2ecfddf417e90efd60b58bcdd1a51ff5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542368"
---
# <span data-ttu-id="84639-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="84639-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="84639-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84639-102">SYNOPSIS</span></span>
<span data-ttu-id="84639-103">Umożliwia zaktualizowanie opisu istniejącego obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="84639-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84639-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84639-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84639-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84639-105">DESCRIPTION</span></span>
<span data-ttu-id="84639-106">Polecenie cmdlet **Set-AzureRmRelayNamespace** umożliwia zaktualizowanie opisu określonego obszaru nazw przekaźnika w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="84639-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="84639-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84639-107">EXAMPLES</span></span>

### <span data-ttu-id="84639-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84639-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="84639-109">Umożliwia zaktualizowanie obszaru nazw przekazywania przy użyciu nowego opisu.</span><span class="sxs-lookup"><span data-stu-id="84639-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="84639-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84639-110">PARAMETERS</span></span>

### <span data-ttu-id="84639-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84639-111">-DefaultProfile</span></span>
<span data-ttu-id="84639-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84639-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84639-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84639-113">-InputObject</span></span>
<span data-ttu-id="84639-114">Obiekt przekazujący obszar nazw</span><span class="sxs-lookup"><span data-stu-id="84639-114">Relay Namespace object</span></span>

```yaml
Type: RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84639-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84639-115">-Name</span></span>
<span data-ttu-id="84639-116">Nazwa obszaru nazw przekaźnika</span><span class="sxs-lookup"><span data-stu-id="84639-116">Relay Namespace Name</span></span>

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

### <span data-ttu-id="84639-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84639-117">-ResourceGroupName</span></span>
<span data-ttu-id="84639-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84639-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="84639-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="84639-119">-Tag</span></span>
<span data-ttu-id="84639-120">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="84639-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="84639-121">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="84639-121">For example:</span></span>

<span data-ttu-id="84639-122">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="84639-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84639-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84639-123">-Confirm</span></span>
<span data-ttu-id="84639-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84639-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84639-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84639-125">-WhatIf</span></span>
<span data-ttu-id="84639-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84639-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84639-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84639-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84639-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84639-128">CommonParameters</span></span>
<span data-ttu-id="84639-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84639-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84639-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84639-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84639-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84639-131">INPUTS</span></span>

### <span data-ttu-id="84639-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84639-132">-ResourceGroupName</span></span>
 <span data-ttu-id="84639-133">System. String</span><span class="sxs-lookup"><span data-stu-id="84639-133">System.String</span></span>

### <span data-ttu-id="84639-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="84639-134">-NamespaceName</span></span>
 <span data-ttu-id="84639-135">System. String</span><span class="sxs-lookup"><span data-stu-id="84639-135">System.String</span></span>

### <span data-ttu-id="84639-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="84639-136">-Location</span></span>
 <span data-ttu-id="84639-137">System. String</span><span class="sxs-lookup"><span data-stu-id="84639-137">System.String</span></span>

### <span data-ttu-id="84639-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="84639-138">-Tag</span></span>
 <span data-ttu-id="84639-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="84639-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="84639-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84639-140">OUTPUTS</span></span>

### <span data-ttu-id="84639-141">Microsoft. Azure. Commands. Relay. modele. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="84639-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="84639-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84639-142">NOTES</span></span>

## <span data-ttu-id="84639-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84639-143">RELATED LINKS</span></span>

