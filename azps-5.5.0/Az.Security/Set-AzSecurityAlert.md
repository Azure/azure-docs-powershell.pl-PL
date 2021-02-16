---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 0555b86b6e5240adfc43bc52153bf14d7612be1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242299"
---
# <span data-ttu-id="f2b7e-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="f2b7e-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="f2b7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b7e-103">Aktualizuje stan alertu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-103">Updates a security alert state.</span></span>

## <span data-ttu-id="f2b7e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2b7e-104">SYNTAX</span></span>

### <span data-ttu-id="f2b7e-105">SubscriptionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f2b7e-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2b7e-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="f2b7e-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2b7e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2b7e-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2b7e-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="f2b7e-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2b7e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2b7e-109">DESCRIPTION</span></span>
<span data-ttu-id="f2b7e-110">Ustawia stan alertu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-110">Sets a security alert state.</span></span>

## <span data-ttu-id="f2b7e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2b7e-111">EXAMPLES</span></span>

### <span data-ttu-id="f2b7e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2b7e-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="f2b7e-113">Odrzuca podniesiony alert zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="f2b7e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2b7e-114">PARAMETERS</span></span>

### <span data-ttu-id="f2b7e-115">- ActionType</span><span class="sxs-lookup"><span data-stu-id="f2b7e-115">-ActionType</span></span>
<span data-ttu-id="f2b7e-116">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-116">Action Type.</span></span>

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

### <span data-ttu-id="f2b7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b7e-117">-DefaultProfile</span></span>
<span data-ttu-id="f2b7e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2b7e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2b7e-119">-InputObject</span></span>
<span data-ttu-id="f2b7e-120">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-120">Input Object.</span></span>

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

### <span data-ttu-id="f2b7e-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f2b7e-121">-Location</span></span>
<span data-ttu-id="f2b7e-122">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-122">Location.</span></span>

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

### <span data-ttu-id="f2b7e-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f2b7e-123">-Name</span></span>
<span data-ttu-id="f2b7e-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-124">Resource name.</span></span>

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

### <span data-ttu-id="f2b7e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2b7e-125">-PassThru</span></span>
<span data-ttu-id="f2b7e-126">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="f2b7e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2b7e-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2b7e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-128">Resource group name.</span></span>

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

### <span data-ttu-id="f2b7e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2b7e-129">-ResourceId</span></span>
<span data-ttu-id="f2b7e-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-130">Resource ID.</span></span>

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

### <span data-ttu-id="f2b7e-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2b7e-131">-Confirm</span></span>
<span data-ttu-id="f2b7e-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b7e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b7e-133">-WhatIf</span></span>
<span data-ttu-id="f2b7e-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2b7e-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b7e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b7e-136">CommonParameters</span></span>
<span data-ttu-id="f2b7e-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2b7e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b7e-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2b7e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b7e-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2b7e-139">INPUTS</span></span>

### <span data-ttu-id="f2b7e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f2b7e-140">System.String</span></span>

### <span data-ttu-id="f2b7e-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="f2b7e-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="f2b7e-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2b7e-142">OUTPUTS</span></span>

### <span data-ttu-id="f2b7e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2b7e-143">System.Boolean</span></span>

## <span data-ttu-id="f2b7e-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2b7e-144">NOTES</span></span>

## <span data-ttu-id="f2b7e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2b7e-145">RELATED LINKS</span></span>
