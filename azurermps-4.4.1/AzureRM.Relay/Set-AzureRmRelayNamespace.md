---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: c243f31ee549443ad959bde13abc9ff3b68c1560
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543023"
---
# <span data-ttu-id="d233e-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="d233e-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="d233e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d233e-102">SYNOPSIS</span></span>
<span data-ttu-id="d233e-103">Umożliwia zaktualizowanie opisu istniejącego obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="d233e-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d233e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d233e-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d233e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d233e-105">DESCRIPTION</span></span>
<span data-ttu-id="d233e-106">Polecenie cmdlet **Set-AzureRmRelayNamespace** umożliwia zaktualizowanie opisu określonego obszaru nazw przekaźnika w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d233e-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="d233e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d233e-107">EXAMPLES</span></span>

### <span data-ttu-id="d233e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d233e-108">Example 1</span></span>
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

<span data-ttu-id="d233e-109">Umożliwia zaktualizowanie obszaru nazw przekazywania przy użyciu nowego opisu.</span><span class="sxs-lookup"><span data-stu-id="d233e-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="d233e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d233e-110">PARAMETERS</span></span>

### <span data-ttu-id="d233e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d233e-111">-ResourceGroupName</span></span>
<span data-ttu-id="d233e-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d233e-112">Resource Group Name.</span></span>

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

### <span data-ttu-id="d233e-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="d233e-113">-Tag</span></span>
<span data-ttu-id="d233e-114">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d233e-114">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d233e-115">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="d233e-115">For example:</span></span>

<span data-ttu-id="d233e-116">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d233e-116">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d233e-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d233e-117">-Confirm</span></span>
<span data-ttu-id="d233e-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d233e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d233e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d233e-119">-WhatIf</span></span>
<span data-ttu-id="d233e-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d233e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d233e-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d233e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d233e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d233e-122">-DefaultProfile</span></span>
<span data-ttu-id="d233e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d233e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d233e-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d233e-124">-InputObject</span></span>
<span data-ttu-id="d233e-125">Obiekt przekazujący obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="d233e-125">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d233e-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d233e-126">-Name</span></span>
<span data-ttu-id="d233e-127">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="d233e-127">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d233e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d233e-128">CommonParameters</span></span>
<span data-ttu-id="d233e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d233e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d233e-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d233e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d233e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d233e-131">INPUTS</span></span>

### <span data-ttu-id="d233e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d233e-132">-ResourceGroupName</span></span>
 <span data-ttu-id="d233e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d233e-133">System.String</span></span>

### <span data-ttu-id="d233e-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d233e-134">-NamespaceName</span></span>
 <span data-ttu-id="d233e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d233e-135">System.String</span></span>

### <span data-ttu-id="d233e-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d233e-136">-Location</span></span>
 <span data-ttu-id="d233e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d233e-137">System.String</span></span>

### <span data-ttu-id="d233e-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="d233e-138">-Tag</span></span>
 <span data-ttu-id="d233e-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d233e-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d233e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d233e-140">OUTPUTS</span></span>

### <span data-ttu-id="d233e-141">Microsoft. Azure. Commands. Relay. modele. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d233e-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="d233e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d233e-142">NOTES</span></span>

## <span data-ttu-id="d233e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d233e-143">RELATED LINKS</span></span>

