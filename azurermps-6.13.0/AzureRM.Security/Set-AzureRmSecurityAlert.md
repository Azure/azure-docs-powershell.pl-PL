---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
ms.openlocfilehash: 81cb94cdcb8efa948160d21da3aca709bb86b6fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543439"
---
# <span data-ttu-id="805aa-101">Set-AzureRmSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="805aa-101">Set-AzureRmSecurityAlert</span></span>

## <span data-ttu-id="805aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="805aa-102">SYNOPSIS</span></span>
<span data-ttu-id="805aa-103">Aktualizuje stan alertu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="805aa-103">Updates a security alert state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="805aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="805aa-104">SYNTAX</span></span>

### <span data-ttu-id="805aa-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="805aa-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="805aa-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="805aa-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="805aa-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="805aa-107">ResourceId</span></span>
```
Set-AzureRmSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="805aa-108">Inputobject</span><span class="sxs-lookup"><span data-stu-id="805aa-108">InputObject</span></span>
```
Set-AzureRmSecurityAlert [-ActionType <String>] -InputObject <PSSetAlertInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="805aa-109">Opis</span><span class="sxs-lookup"><span data-stu-id="805aa-109">DESCRIPTION</span></span>
<span data-ttu-id="805aa-110">Ustawia stan alertu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="805aa-110">Sets a security alert state.</span></span>

## <span data-ttu-id="805aa-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="805aa-111">EXAMPLES</span></span>

### <span data-ttu-id="805aa-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="805aa-112">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="805aa-113">Odrzucanie zgłoszonego alertu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="805aa-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="805aa-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="805aa-114">PARAMETERS</span></span>

### <span data-ttu-id="805aa-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="805aa-115">-ActionType</span></span>
<span data-ttu-id="805aa-116">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="805aa-116">Action Type.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="805aa-117">-DefaultProfile</span></span>
<span data-ttu-id="805aa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="805aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="805aa-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="805aa-119">-InputObject</span></span>
<span data-ttu-id="805aa-120">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="805aa-120">Input Object.</span></span>

```yaml
Type: PSSetAlertInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="805aa-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="805aa-121">-Location</span></span>
<span data-ttu-id="805aa-122">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="805aa-122">Location.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805aa-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="805aa-123">-Name</span></span>
<span data-ttu-id="805aa-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="805aa-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805aa-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="805aa-125">-PassThru</span></span>
<span data-ttu-id="805aa-126">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="805aa-126">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805aa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="805aa-127">-ResourceGroupName</span></span>
<span data-ttu-id="805aa-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="805aa-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805aa-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="805aa-129">-ResourceId</span></span>
<span data-ttu-id="805aa-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="805aa-130">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805aa-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="805aa-131">-Confirm</span></span>
<span data-ttu-id="805aa-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="805aa-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805aa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="805aa-133">-WhatIf</span></span>
<span data-ttu-id="805aa-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="805aa-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="805aa-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="805aa-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805aa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="805aa-136">CommonParameters</span></span>
<span data-ttu-id="805aa-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="805aa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="805aa-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="805aa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="805aa-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="805aa-139">INPUTS</span></span>

### <span data-ttu-id="805aa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="805aa-140">System.String</span></span>
<span data-ttu-id="805aa-141">Microsoft. Azure. Commands. Security. cmdlet. Alerts. PSSetAlertInputObject</span><span class="sxs-lookup"><span data-stu-id="805aa-141">Microsoft.Azure.Commands.Security.Cmdlets.Alerts.PSSetAlertInputObject</span></span>

## <span data-ttu-id="805aa-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="805aa-142">OUTPUTS</span></span>

### <span data-ttu-id="805aa-143">Microsoft. Azure. Commands. Security. models. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="805aa-143">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="805aa-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="805aa-144">NOTES</span></span>

## <span data-ttu-id="805aa-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="805aa-145">RELATED LINKS</span></span>
