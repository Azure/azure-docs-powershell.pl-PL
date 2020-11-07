---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 1c6f6a38c1811bdda32b60d4af1707c78eb7afd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717051"
---
# <span data-ttu-id="6bcb7-101">Remove-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="6bcb7-101">Remove-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="6bcb7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6bcb7-102">SYNOPSIS</span></span>
<span data-ttu-id="6bcb7-103">Usuwa ustawienia obszaru roboczego zabezpieczeń dla tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-103">Deletes the security workspace setting for this subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bcb7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6bcb7-104">SYNTAX</span></span>

### <span data-ttu-id="6bcb7-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6bcb7-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bcb7-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="6bcb7-106">ResourceId</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bcb7-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="6bcb7-107">InputObject</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -InputObject <PSRemoveWorkspaceSettingInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bcb7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6bcb7-108">DESCRIPTION</span></span>
<span data-ttu-id="6bcb7-109">Usuwa ustawienia obszaru roboczego zabezpieczeń dla tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="6bcb7-110">Ta czynność spowoduje, że nowo zainstalowani agenci zabezpieczeń będą mogli raportować domyślny obszar roboczy tego susbscription.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-110">This action will make the newly installed security agents to report to the default workspace of this susbscription.</span></span>

## <span data-ttu-id="6bcb7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6bcb7-111">EXAMPLES</span></span>

### <span data-ttu-id="6bcb7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6bcb7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="6bcb7-113">Usuwa ustawienia obszaru roboczego zabezpieczeń dla tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="6bcb7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bcb7-114">PARAMETERS</span></span>

### <span data-ttu-id="6bcb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bcb7-115">-DefaultProfile</span></span>
<span data-ttu-id="6bcb7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bcb7-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6bcb7-117">-InputObject</span></span>
<span data-ttu-id="6bcb7-118">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-118">Input Object.</span></span>

```yaml
Type: PSRemoveWorkspaceSettingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6bcb7-119">-Name</span></span>
<span data-ttu-id="6bcb7-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-120">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bcb7-121">-PassThru</span></span>
<span data-ttu-id="6bcb7-122">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="6bcb7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bcb7-123">-ResourceId</span></span>
<span data-ttu-id="6bcb7-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-124">Resource ID.</span></span>

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

### <span data-ttu-id="6bcb7-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6bcb7-125">-Confirm</span></span>
<span data-ttu-id="6bcb7-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bcb7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bcb7-127">-WhatIf</span></span>
<span data-ttu-id="6bcb7-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bcb7-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bcb7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bcb7-130">CommonParameters</span></span>
<span data-ttu-id="6bcb7-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bcb7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bcb7-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bcb7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bcb7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bcb7-133">INPUTS</span></span>

### <span data-ttu-id="6bcb7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6bcb7-134">System.String</span></span>
<span data-ttu-id="6bcb7-135">Microsoft. Azure. polecenia. Security. cmdlets. WorkspaceSettings. PSRemoveWorkspaceSettingInputObject</span><span class="sxs-lookup"><span data-stu-id="6bcb7-135">Microsoft.Azure.Commands.Security.Cmdlets.WorkspaceSettings.PSRemoveWorkspaceSettingInputObject</span></span>

## <span data-ttu-id="6bcb7-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6bcb7-136">OUTPUTS</span></span>

### <span data-ttu-id="6bcb7-137">Microsoft. Azure. Commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="6bcb7-137">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="6bcb7-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6bcb7-138">NOTES</span></span>

## <span data-ttu-id="6bcb7-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bcb7-139">RELATED LINKS</span></span>
