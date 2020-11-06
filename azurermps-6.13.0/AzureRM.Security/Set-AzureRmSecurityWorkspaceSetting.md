---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 3d2fdd8b6a1763aea97da3967fb2696857e7fd75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548568"
---
# <span data-ttu-id="604fe-101">Set-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="604fe-101">Set-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="604fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="604fe-102">SYNOPSIS</span></span>
<span data-ttu-id="604fe-103">Aktualizuje ustawienia obszaru roboczego dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="604fe-103">Updates the workspace settings for the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="604fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="604fe-104">SYNTAX</span></span>

```
Set-AzureRmSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="604fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="604fe-105">DESCRIPTION</span></span>
<span data-ttu-id="604fe-106">Aktualizuje ustawienia obszaru roboczego dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="604fe-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="604fe-107">W skonfigurowanym obszarze roboczym będą przechowywane dane zabezpieczeń, które zostały pobrane przez agenta zabezpieczeń zainstalowanego na maszynach wirtualnych w ramach tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="604fe-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="604fe-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="604fe-108">EXAMPLES</span></span>

### <span data-ttu-id="604fe-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="604fe-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="604fe-110">Umożliwia ustawienie obszaru roboczego "Mój obszar roboczy" w celu zablokowania wszystkich danych zabezpieczeń, które zostały pobrane przez agentów zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="604fe-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="604fe-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="604fe-111">PARAMETERS</span></span>

### <span data-ttu-id="604fe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="604fe-112">-DefaultProfile</span></span>
<span data-ttu-id="604fe-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="604fe-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="604fe-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="604fe-114">-Name</span></span>
<span data-ttu-id="604fe-115">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="604fe-115">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="604fe-116">-Zakres</span><span class="sxs-lookup"><span data-stu-id="604fe-116">-Scope</span></span>
<span data-ttu-id="604fe-117">Objęt.</span><span class="sxs-lookup"><span data-stu-id="604fe-117">Scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="604fe-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="604fe-118">-WorkspaceId</span></span>
<span data-ttu-id="604fe-119">Identyfikator obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="604fe-119">Workspace ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604fe-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="604fe-120">-Confirm</span></span>
<span data-ttu-id="604fe-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="604fe-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="604fe-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="604fe-122">-WhatIf</span></span>
<span data-ttu-id="604fe-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="604fe-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="604fe-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="604fe-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="604fe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="604fe-125">CommonParameters</span></span>
<span data-ttu-id="604fe-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="604fe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="604fe-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="604fe-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="604fe-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="604fe-128">INPUTS</span></span>

### <span data-ttu-id="604fe-129">System. String</span><span class="sxs-lookup"><span data-stu-id="604fe-129">System.String</span></span>

## <span data-ttu-id="604fe-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="604fe-130">OUTPUTS</span></span>

### <span data-ttu-id="604fe-131">Microsoft. Azure. Commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="604fe-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="604fe-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="604fe-132">NOTES</span></span>

## <span data-ttu-id="604fe-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="604fe-133">RELATED LINKS</span></span>
