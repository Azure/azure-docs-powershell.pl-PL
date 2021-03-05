---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: 313022f4d622058594398b72dfd917e18cfaec77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978122"
---
# <span data-ttu-id="4d536-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4d536-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="4d536-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d536-102">SYNOPSIS</span></span>
<span data-ttu-id="4d536-103">Generuje tolen SAS dla reguły autoryzacji usługi Azure Servicebus przestrzeni nazw/kolejki/tematu.</span><span class="sxs-lookup"><span data-stu-id="4d536-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="4d536-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4d536-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d536-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4d536-105">DESCRIPTION</span></span>
<span data-ttu-id="4d536-106">Polecenie New-AzServiceBusAuthorizationRuleSASToken cmdlet generuje token SAS (Shared Access Signature) dla usługi Azure Eventhub Namesapce lub Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="4d536-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="4d536-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4d536-107">EXAMPLES</span></span>

### <span data-ttu-id="4d536-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4d536-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="4d536-109">Wygeneruj token SAS dla danej reguły autoryzacji dla przestrzeni nazw z czasem rozpoczęcia i wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="4d536-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="4d536-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4d536-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="4d536-111">Wygeneruj token SAS dla danej reguły autoryzacji dla przestrzeni nazw z czasem wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="4d536-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="4d536-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d536-112">PARAMETERS</span></span>

### <span data-ttu-id="4d536-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="4d536-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="4d536-114">ARM ResourceId reguły autoryzowania</span><span class="sxs-lookup"><span data-stu-id="4d536-114">ARM ResourceId of the Authoraization Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d536-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d536-115">-DefaultProfile</span></span>
<span data-ttu-id="4d536-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d536-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d536-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4d536-117">-ExpiryTime</span></span>
<span data-ttu-id="4d536-118">Czas wygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="4d536-118">Expiry Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d536-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4d536-119">-KeyType</span></span>
<span data-ttu-id="4d536-120">Typ klucza</span><span class="sxs-lookup"><span data-stu-id="4d536-120">Key Type</span></span>

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

### <span data-ttu-id="4d536-121">— StartTime</span><span class="sxs-lookup"><span data-stu-id="4d536-121">-StartTime</span></span>
<span data-ttu-id="4d536-122">Godzina rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="4d536-122">Start Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d536-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d536-123">-Confirm</span></span>
<span data-ttu-id="4d536-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4d536-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d536-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d536-125">-WhatIf</span></span>
<span data-ttu-id="4d536-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d536-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d536-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4d536-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d536-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d536-128">CommonParameters</span></span>
<span data-ttu-id="4d536-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d536-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4d536-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d536-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d536-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d536-131">INPUTS</span></span>

### <span data-ttu-id="4d536-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4d536-132">System.String</span></span>

### <span data-ttu-id="4d536-133">System.Nullable'1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4d536-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4d536-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d536-134">OUTPUTS</span></span>

### <span data-ttu-id="4d536-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="4d536-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="4d536-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4d536-136">NOTES</span></span>

## <span data-ttu-id="4d536-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d536-137">RELATED LINKS</span></span>