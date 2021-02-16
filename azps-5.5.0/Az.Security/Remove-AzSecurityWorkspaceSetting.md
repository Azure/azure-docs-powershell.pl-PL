---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183586"
---
# <span data-ttu-id="87acc-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="87acc-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="87acc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87acc-102">SYNOPSIS</span></span>
<span data-ttu-id="87acc-103">Usuwa ustawienie obszaru roboczego zabezpieczeń dla tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87acc-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="87acc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="87acc-104">SYNTAX</span></span>

### <span data-ttu-id="87acc-105">SubscriptionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="87acc-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87acc-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="87acc-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87acc-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="87acc-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87acc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="87acc-108">DESCRIPTION</span></span>
<span data-ttu-id="87acc-109">Usuwa ustawienie obszaru roboczego zabezpieczeń dla tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87acc-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="87acc-110">Ta akcja spowoduje, że nowo zainstalowani agenci zabezpieczeń będą raportować w domyślnym obszarze roboczym tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87acc-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="87acc-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="87acc-111">EXAMPLES</span></span>

### <span data-ttu-id="87acc-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87acc-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="87acc-113">Usuwa ustawienie obszaru roboczego zabezpieczeń dla tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87acc-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="87acc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87acc-114">PARAMETERS</span></span>

### <span data-ttu-id="87acc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87acc-115">-DefaultProfile</span></span>
<span data-ttu-id="87acc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="87acc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87acc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87acc-117">-InputObject</span></span>
<span data-ttu-id="87acc-118">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="87acc-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87acc-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="87acc-119">-Name</span></span>
<span data-ttu-id="87acc-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="87acc-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87acc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87acc-121">-PassThru</span></span>
<span data-ttu-id="87acc-122">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="87acc-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="87acc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87acc-123">-ResourceId</span></span>
<span data-ttu-id="87acc-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="87acc-124">Resource ID.</span></span>

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

### <span data-ttu-id="87acc-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87acc-125">-Confirm</span></span>
<span data-ttu-id="87acc-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="87acc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87acc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87acc-127">-WhatIf</span></span>
<span data-ttu-id="87acc-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87acc-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87acc-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="87acc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87acc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87acc-130">CommonParameters</span></span>
<span data-ttu-id="87acc-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87acc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87acc-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87acc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87acc-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87acc-133">INPUTS</span></span>

### <span data-ttu-id="87acc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="87acc-134">System.String</span></span>

### <span data-ttu-id="87acc-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="87acc-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="87acc-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87acc-136">OUTPUTS</span></span>

### <span data-ttu-id="87acc-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="87acc-137">System.Boolean</span></span>

## <span data-ttu-id="87acc-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="87acc-138">NOTES</span></span>

## <span data-ttu-id="87acc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87acc-139">RELATED LINKS</span></span>
