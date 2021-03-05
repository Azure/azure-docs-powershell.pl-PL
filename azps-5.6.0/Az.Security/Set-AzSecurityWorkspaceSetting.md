---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 6bcee25399004d5fb8f485e9c58446713bedc5c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005729"
---
# <span data-ttu-id="74644-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="74644-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="74644-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74644-102">SYNOPSIS</span></span>
<span data-ttu-id="74644-103">Aktualizuje ustawienia obszaru roboczego dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="74644-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="74644-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74644-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74644-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="74644-105">DESCRIPTION</span></span>
<span data-ttu-id="74644-106">Aktualizuje ustawienia obszaru roboczego dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="74644-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="74644-107">Skonfigurowany obszar roboczy będzie zawierać dane zabezpieczeń, które zostały zebrane przez agenta agenta Azure Log Analytics zainstalowanego w maszyny wirtualnej w ramach tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="74644-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="74644-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74644-108">EXAMPLES</span></span>

### <span data-ttu-id="74644-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74644-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="74644-110">Ustawia obszar roboczy "securityuserws" tak, aby zawierał wszystkie dane zabezpieczeń, które zostały zebrane przez agenta usługi Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="74644-110">Sets the "securityuserws" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="74644-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74644-111">PARAMETERS</span></span>

### <span data-ttu-id="74644-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74644-112">-DefaultProfile</span></span>
<span data-ttu-id="74644-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74644-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74644-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74644-114">-Name</span></span>
<span data-ttu-id="74644-115">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="74644-115">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74644-116">— Zakres</span><span class="sxs-lookup"><span data-stu-id="74644-116">-Scope</span></span>
<span data-ttu-id="74644-117">Zakres.</span><span class="sxs-lookup"><span data-stu-id="74644-117">Scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74644-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="74644-118">-WorkspaceId</span></span>
<span data-ttu-id="74644-119">Identyfikator obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="74644-119">Workspace ID.</span></span>

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

### <span data-ttu-id="74644-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74644-120">-Confirm</span></span>
<span data-ttu-id="74644-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74644-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74644-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74644-122">-WhatIf</span></span>
<span data-ttu-id="74644-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74644-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74644-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="74644-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74644-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74644-125">CommonParameters</span></span>
<span data-ttu-id="74644-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74644-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74644-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74644-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74644-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74644-128">INPUTS</span></span>

### <span data-ttu-id="74644-129">System.String</span><span class="sxs-lookup"><span data-stu-id="74644-129">System.String</span></span>

## <span data-ttu-id="74644-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74644-130">OUTPUTS</span></span>

### <span data-ttu-id="74644-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="74644-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="74644-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74644-132">NOTES</span></span>

## <span data-ttu-id="74644-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74644-133">RELATED LINKS</span></span>
