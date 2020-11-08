---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 79780c101296d78115a1c88ef4d4aebcd3721c22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050549"
---
# <span data-ttu-id="3b808-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="3b808-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="3b808-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b808-102">SYNOPSIS</span></span>
<span data-ttu-id="3b808-103">Usuwa ustawienia obszaru roboczego zabezpieczeń dla tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3b808-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="3b808-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b808-104">SYNTAX</span></span>

### <span data-ttu-id="3b808-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3b808-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b808-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="3b808-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b808-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b808-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b808-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3b808-108">DESCRIPTION</span></span>
<span data-ttu-id="3b808-109">Usuwa ustawienia obszaru roboczego zabezpieczeń dla tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3b808-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="3b808-110">Ta czynność spowoduje, że nowo zainstalowani agenci zabezpieczeń będą mogli raportować domyślny obszar roboczy tego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="3b808-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="3b808-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b808-111">EXAMPLES</span></span>

### <span data-ttu-id="3b808-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b808-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="3b808-113">Usuwa ustawienia obszaru roboczego zabezpieczeń dla tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3b808-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="3b808-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b808-114">PARAMETERS</span></span>

### <span data-ttu-id="3b808-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b808-115">-DefaultProfile</span></span>
<span data-ttu-id="3b808-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b808-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b808-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b808-117">-InputObject</span></span>
<span data-ttu-id="3b808-118">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="3b808-118">Input Object.</span></span>

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

### <span data-ttu-id="3b808-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b808-119">-Name</span></span>
<span data-ttu-id="3b808-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3b808-120">Resource name.</span></span>

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

### <span data-ttu-id="3b808-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b808-121">-PassThru</span></span>
<span data-ttu-id="3b808-122">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="3b808-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="3b808-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b808-123">-ResourceId</span></span>
<span data-ttu-id="3b808-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3b808-124">Resource ID.</span></span>

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

### <span data-ttu-id="3b808-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b808-125">-Confirm</span></span>
<span data-ttu-id="3b808-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b808-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b808-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b808-127">-WhatIf</span></span>
<span data-ttu-id="3b808-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b808-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b808-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b808-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b808-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b808-130">CommonParameters</span></span>
<span data-ttu-id="3b808-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b808-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b808-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b808-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b808-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b808-133">INPUTS</span></span>

### <span data-ttu-id="3b808-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3b808-134">System.String</span></span>

### <span data-ttu-id="3b808-135">Microsoft. Azure. Commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="3b808-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="3b808-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b808-136">OUTPUTS</span></span>

### <span data-ttu-id="3b808-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b808-137">System.Boolean</span></span>

## <span data-ttu-id="3b808-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b808-138">NOTES</span></span>

## <span data-ttu-id="3b808-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b808-139">RELATED LINKS</span></span>
