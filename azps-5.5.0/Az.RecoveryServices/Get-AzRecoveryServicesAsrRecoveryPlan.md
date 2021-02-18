---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202043"
---
# <span data-ttu-id="d8f31-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d8f31-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="d8f31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f31-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f31-103">Pobiera plan odzyskiwania lub wszystkie plany odzyskiwania w magazynie usług odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="d8f31-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="d8f31-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8f31-104">SYNTAX</span></span>

### <span data-ttu-id="d8f31-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d8f31-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8f31-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d8f31-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8f31-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d8f31-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8f31-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8f31-108">DESCRIPTION</span></span>
<span data-ttu-id="d8f31-109">Polecenie **cmdlet Get-AzRecoveryServicesAsrRecoveryPlan** pobiera szczegóły określonego planu odzyskiwania lub wszystkich planów odzyskiwania w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d8f31-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="d8f31-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8f31-110">EXAMPLES</span></span>

### <span data-ttu-id="d8f31-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d8f31-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="d8f31-112">Pobiera plan odzyskiwania pod określoną nazwą.</span><span class="sxs-lookup"><span data-stu-id="d8f31-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="d8f31-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8f31-113">PARAMETERS</span></span>

### <span data-ttu-id="d8f31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f31-114">-DefaultProfile</span></span>
<span data-ttu-id="d8f31-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f31-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d8f31-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d8f31-116">-FriendlyName</span></span>
<span data-ttu-id="d8f31-117">Określa przyjazną nazwę planu odzyskiwania, który ma być uzyskać.</span><span class="sxs-lookup"><span data-stu-id="d8f31-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f31-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d8f31-118">-Name</span></span>
<span data-ttu-id="d8f31-119">Określa nazwę planu odzyskiwania, który ma być uzyskać.</span><span class="sxs-lookup"><span data-stu-id="d8f31-119">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f31-120">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="d8f31-120">-Path</span></span>
<span data-ttu-id="d8f31-121">Określa ścieżkę pliku, w której to polecenie cmdlet zapisuje definicję json planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d8f31-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="d8f31-122">Definicję json można edytować w celu zmodyfikowania planu odzyskiwania i używać jej do aktualizowania planu odzyskiwania za pomocą Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span><span class="sxs-lookup"><span data-stu-id="d8f31-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f31-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f31-123">CommonParameters</span></span>
<span data-ttu-id="d8f31-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f31-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f31-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8f31-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f31-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8f31-126">INPUTS</span></span>

### <span data-ttu-id="d8f31-127">Brak</span><span class="sxs-lookup"><span data-stu-id="d8f31-127">None</span></span>

## <span data-ttu-id="d8f31-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8f31-128">OUTPUTS</span></span>

### <span data-ttu-id="d8f31-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d8f31-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="d8f31-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8f31-130">NOTES</span></span>

## <span data-ttu-id="d8f31-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8f31-131">RELATED LINKS</span></span>

[<span data-ttu-id="d8f31-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d8f31-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d8f31-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d8f31-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d8f31-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d8f31-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
