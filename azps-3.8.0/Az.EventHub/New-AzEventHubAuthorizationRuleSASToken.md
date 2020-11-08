---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 24348c44ef9b529507c50a689f181739d1474e22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051128"
---
# <span data-ttu-id="57e6b-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="57e6b-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="57e6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="57e6b-103">Generuje token SAS dla reguły autoryzacji usługi Azure eventhub w obszarze nazw/eventhub.</span><span class="sxs-lookup"><span data-stu-id="57e6b-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="57e6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57e6b-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57e6b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="57e6b-105">DESCRIPTION</span></span>
<span data-ttu-id="57e6b-106">Polecenie cmdlet New-AzEventHubAuthorizationRuleSASToken generuje token dostępu współużytkowanego (SAS) dla usługi Azure Eventhub Namesapce lub Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="57e6b-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="57e6b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57e6b-107">EXAMPLES</span></span>

### <span data-ttu-id="57e6b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57e6b-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="57e6b-109">Generuj token SAS dla danej reguły authorixation dla obszaru nazw z godziną rozpoczęcia i upływem czasu...</span><span class="sxs-lookup"><span data-stu-id="57e6b-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="57e6b-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="57e6b-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="57e6b-111">Generuj token SAS dla danej reguły authorixation dla obszaru nazw z upływem czasu wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="57e6b-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="57e6b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57e6b-112">PARAMETERS</span></span>

### <span data-ttu-id="57e6b-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="57e6b-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="57e6b-114">Identyfikator zasobu ARM reguły Authoraization</span><span class="sxs-lookup"><span data-stu-id="57e6b-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="57e6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e6b-115">-DefaultProfile</span></span>
<span data-ttu-id="57e6b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57e6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57e6b-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="57e6b-117">-ExpiryTime</span></span>
<span data-ttu-id="57e6b-118">Czas wygaśnięcia</span><span class="sxs-lookup"><span data-stu-id="57e6b-118">Expiry Time</span></span>

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

### <span data-ttu-id="57e6b-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="57e6b-119">-KeyType</span></span>
<span data-ttu-id="57e6b-120">Typ klucza</span><span class="sxs-lookup"><span data-stu-id="57e6b-120">Key Type</span></span>

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

### <span data-ttu-id="57e6b-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="57e6b-121">-StartTime</span></span>
<span data-ttu-id="57e6b-122">Godzina rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="57e6b-122">Start Time</span></span>

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

### <span data-ttu-id="57e6b-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57e6b-123">-Confirm</span></span>
<span data-ttu-id="57e6b-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57e6b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57e6b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57e6b-125">-WhatIf</span></span>
<span data-ttu-id="57e6b-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57e6b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57e6b-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57e6b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57e6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e6b-128">CommonParameters</span></span>
<span data-ttu-id="57e6b-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57e6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="57e6b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57e6b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e6b-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57e6b-131">INPUTS</span></span>

### <span data-ttu-id="57e6b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="57e6b-132">System.String</span></span>

### <span data-ttu-id="57e6b-133">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="57e6b-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="57e6b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57e6b-134">OUTPUTS</span></span>

### <span data-ttu-id="57e6b-135">Microsoft. Azure. Commands. EventHub. modele. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="57e6b-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="57e6b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57e6b-136">NOTES</span></span>

## <span data-ttu-id="57e6b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57e6b-137">RELATED LINKS</span></span>
