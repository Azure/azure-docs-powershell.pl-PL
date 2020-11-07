---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: eb42dc22f972928405821e8468e5610fa9c4514f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708450"
---
# <span data-ttu-id="be5a1-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="be5a1-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="be5a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be5a1-102">SYNOPSIS</span></span>
<span data-ttu-id="be5a1-103">Umożliwia zaktualizowanie opisu istniejącego obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="be5a1-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="be5a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be5a1-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be5a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="be5a1-105">DESCRIPTION</span></span>
<span data-ttu-id="be5a1-106">Polecenie cmdlet **Set-AzRelayNamespace** umożliwia zaktualizowanie opisu określonego obszaru nazw przekaźnika w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="be5a1-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="be5a1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be5a1-107">EXAMPLES</span></span>

### <span data-ttu-id="be5a1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="be5a1-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="be5a1-109">Umożliwia zaktualizowanie obszaru nazw przekazywania przy użyciu nowego opisu.</span><span class="sxs-lookup"><span data-stu-id="be5a1-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="be5a1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be5a1-110">PARAMETERS</span></span>

### <span data-ttu-id="be5a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be5a1-111">-DefaultProfile</span></span>
<span data-ttu-id="be5a1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be5a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be5a1-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="be5a1-113">-InputObject</span></span>
<span data-ttu-id="be5a1-114">Obiekt przekazujący obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="be5a1-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="be5a1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be5a1-115">-Name</span></span>
<span data-ttu-id="be5a1-116">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="be5a1-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="be5a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be5a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="be5a1-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be5a1-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="be5a1-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="be5a1-119">-Tag</span></span>
<span data-ttu-id="be5a1-120">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="be5a1-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="be5a1-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be5a1-121">-Confirm</span></span>
<span data-ttu-id="be5a1-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be5a1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5a1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be5a1-123">-WhatIf</span></span>
<span data-ttu-id="be5a1-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be5a1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be5a1-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="be5a1-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5a1-126">CommonParameters</span></span>
<span data-ttu-id="be5a1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be5a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5a1-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be5a1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5a1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be5a1-129">INPUTS</span></span>

### <span data-ttu-id="be5a1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="be5a1-130">System.String</span></span>

### <span data-ttu-id="be5a1-131">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="be5a1-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="be5a1-132">Microsoft. Azure. Commands. Relay. modele. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="be5a1-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="be5a1-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be5a1-133">OUTPUTS</span></span>

### <span data-ttu-id="be5a1-134">Microsoft. Azure. Commands. Relay. modele. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="be5a1-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="be5a1-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be5a1-135">NOTES</span></span>

## <span data-ttu-id="be5a1-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be5a1-136">RELATED LINKS</span></span>