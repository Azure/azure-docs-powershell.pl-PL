---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: c9ed93f1a55f7c8cc52bef68d306f7d246d595a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873179"
---
# <span data-ttu-id="3ce1b-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="3ce1b-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="3ce1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ce1b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce1b-103">Aktualizuje stan alertu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-103">Updates a security alert state.</span></span>

## <span data-ttu-id="3ce1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ce1b-104">SYNTAX</span></span>

### <span data-ttu-id="3ce1b-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3ce1b-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce1b-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="3ce1b-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce1b-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="3ce1b-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce1b-108">Inputobject</span><span class="sxs-lookup"><span data-stu-id="3ce1b-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ce1b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3ce1b-109">DESCRIPTION</span></span>
<span data-ttu-id="3ce1b-110">Ustawia stan alertu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-110">Sets a security alert state.</span></span>

## <span data-ttu-id="3ce1b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ce1b-111">EXAMPLES</span></span>

### <span data-ttu-id="3ce1b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3ce1b-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="3ce1b-113">Odrzucanie zgłoszonego alertu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="3ce1b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ce1b-114">PARAMETERS</span></span>

### <span data-ttu-id="3ce1b-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="3ce1b-115">-ActionType</span></span>
<span data-ttu-id="3ce1b-116">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce1b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce1b-117">-DefaultProfile</span></span>
<span data-ttu-id="3ce1b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ce1b-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3ce1b-119">-InputObject</span></span>
<span data-ttu-id="3ce1b-120">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce1b-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3ce1b-121">-Location</span></span>
<span data-ttu-id="3ce1b-122">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce1b-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3ce1b-123">-Name</span></span>
<span data-ttu-id="3ce1b-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce1b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ce1b-125">-PassThru</span></span>
<span data-ttu-id="3ce1b-126">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-126">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce1b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce1b-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ce1b-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce1b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ce1b-129">-ResourceId</span></span>
<span data-ttu-id="3ce1b-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-130">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce1b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3ce1b-131">-Confirm</span></span>
<span data-ttu-id="3ce1b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ce1b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce1b-133">-WhatIf</span></span>
<span data-ttu-id="3ce1b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ce1b-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ce1b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce1b-136">CommonParameters</span></span>
<span data-ttu-id="3ce1b-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ce1b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce1b-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce1b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce1b-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ce1b-139">INPUTS</span></span>

### <span data-ttu-id="3ce1b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3ce1b-140">System.String</span></span>

### <span data-ttu-id="3ce1b-141">Microsoft. Azure. Commands. Security. models. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="3ce1b-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="3ce1b-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ce1b-142">OUTPUTS</span></span>

### <span data-ttu-id="3ce1b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ce1b-143">System.Boolean</span></span>

## <span data-ttu-id="3ce1b-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ce1b-144">NOTES</span></span>

## <span data-ttu-id="3ce1b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ce1b-145">RELATED LINKS</span></span>
