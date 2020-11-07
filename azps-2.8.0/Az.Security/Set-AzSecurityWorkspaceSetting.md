---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: c425a7d11fab8bc019ca3944d034dfa2bfb96d06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873175"
---
# <span data-ttu-id="c319d-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="c319d-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="c319d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c319d-102">SYNOPSIS</span></span>
<span data-ttu-id="c319d-103">Aktualizuje ustawienia obszaru roboczego dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c319d-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="c319d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c319d-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c319d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c319d-105">DESCRIPTION</span></span>
<span data-ttu-id="c319d-106">Aktualizuje ustawienia obszaru roboczego dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c319d-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="c319d-107">W skonfigurowanym obszarze roboczym zostaną umieszczone dane zabezpieczeń, które zostały zebrane przez agenta usługi Analiza dzienników Azure zainstalowaną na maszynach wirtualnych w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c319d-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="c319d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c319d-108">EXAMPLES</span></span>

### <span data-ttu-id="c319d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c319d-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="c319d-110">Umożliwia ustawienie obszaru roboczego "Mój obszar roboczy" w celu zablokowania wszystkich danych zabezpieczeń zebranych przez agenta analizy dzienników usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="c319d-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="c319d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c319d-111">PARAMETERS</span></span>

### <span data-ttu-id="c319d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c319d-112">-DefaultProfile</span></span>
<span data-ttu-id="c319d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c319d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c319d-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c319d-114">-Name</span></span>
<span data-ttu-id="c319d-115">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c319d-115">Resource name.</span></span>

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

### <span data-ttu-id="c319d-116">-Zakres</span><span class="sxs-lookup"><span data-stu-id="c319d-116">-Scope</span></span>
<span data-ttu-id="c319d-117">Objęt.</span><span class="sxs-lookup"><span data-stu-id="c319d-117">Scope.</span></span>

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

### <span data-ttu-id="c319d-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="c319d-118">-WorkspaceId</span></span>
<span data-ttu-id="c319d-119">Identyfikator obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c319d-119">Workspace ID.</span></span>

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

### <span data-ttu-id="c319d-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c319d-120">-Confirm</span></span>
<span data-ttu-id="c319d-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c319d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c319d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c319d-122">-WhatIf</span></span>
<span data-ttu-id="c319d-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c319d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c319d-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c319d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c319d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c319d-125">CommonParameters</span></span>
<span data-ttu-id="c319d-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c319d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c319d-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c319d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c319d-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c319d-128">INPUTS</span></span>

### <span data-ttu-id="c319d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c319d-129">System.String</span></span>

## <span data-ttu-id="c319d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c319d-130">OUTPUTS</span></span>

### <span data-ttu-id="c319d-131">Microsoft. Azure. Commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="c319d-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="c319d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c319d-132">NOTES</span></span>

## <span data-ttu-id="c319d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c319d-133">RELATED LINKS</span></span>
