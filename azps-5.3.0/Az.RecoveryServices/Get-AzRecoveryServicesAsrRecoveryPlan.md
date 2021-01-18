---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501385"
---
# <span data-ttu-id="c2d92-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c2d92-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="c2d92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2d92-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d92-103">Pobiera plan odzyskiwania lub wszystkie plany odzyskiwania w magazynie usług Recovery Services</span><span class="sxs-lookup"><span data-stu-id="c2d92-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="c2d92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2d92-104">SYNTAX</span></span>

### <span data-ttu-id="c2d92-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c2d92-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d92-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c2d92-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d92-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c2d92-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2d92-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c2d92-108">DESCRIPTION</span></span>
<span data-ttu-id="c2d92-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan** pobiera szczegóły określonego planu odzyskiwania lub wszystkich planów odzyskiwania w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="c2d92-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="c2d92-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2d92-110">EXAMPLES</span></span>

### <span data-ttu-id="c2d92-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2d92-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="c2d92-112">Pobiera plan odzyskiwania o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="c2d92-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="c2d92-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2d92-113">PARAMETERS</span></span>

### <span data-ttu-id="c2d92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d92-114">-DefaultProfile</span></span>
<span data-ttu-id="c2d92-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2d92-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c2d92-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c2d92-116">-FriendlyName</span></span>
<span data-ttu-id="c2d92-117">Określa przyjazną nazwę planu odzyskiwania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="c2d92-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="c2d92-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2d92-118">-Name</span></span>
<span data-ttu-id="c2d92-119">Określa nazwę planu odzyskiwania, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="c2d92-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="c2d92-120">-Path</span><span class="sxs-lookup"><span data-stu-id="c2d92-120">-Path</span></span>
<span data-ttu-id="c2d92-121">Określa ścieżkę pliku, do którego to polecenie cmdlet zapisuje definicję JSON planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c2d92-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="c2d92-122">Definicję JSON można edytować w celu zmodyfikowania planu odzyskiwania i użycia w celu zaktualizowania planu odzyskiwania za pomocą polecenia cmdlet Update-AzRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c2d92-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="c2d92-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d92-123">CommonParameters</span></span>
<span data-ttu-id="c2d92-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2d92-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d92-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2d92-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d92-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2d92-126">INPUTS</span></span>

### <span data-ttu-id="c2d92-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c2d92-127">None</span></span>

## <span data-ttu-id="c2d92-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2d92-128">OUTPUTS</span></span>

### <span data-ttu-id="c2d92-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c2d92-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="c2d92-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2d92-130">NOTES</span></span>

## <span data-ttu-id="c2d92-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2d92-131">RELATED LINKS</span></span>

[<span data-ttu-id="c2d92-132">Nowe — AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c2d92-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c2d92-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c2d92-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c2d92-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c2d92-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
