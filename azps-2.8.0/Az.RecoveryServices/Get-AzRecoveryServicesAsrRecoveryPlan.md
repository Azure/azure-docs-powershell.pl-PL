---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 8c4bc3598d18042d31e98b37d9fc2c09d45b74d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872748"
---
# <span data-ttu-id="a8a56-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8a56-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="a8a56-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8a56-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a56-103">Pobiera plan odzyskiwania lub wszystkie plany odzyskiwania w magazynie usług Recovery Services</span><span class="sxs-lookup"><span data-stu-id="a8a56-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="a8a56-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8a56-104">SYNTAX</span></span>

### <span data-ttu-id="a8a56-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a8a56-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8a56-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a8a56-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8a56-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a8a56-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8a56-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a8a56-108">DESCRIPTION</span></span>
<span data-ttu-id="a8a56-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan** pobiera szczegóły określonego planu odzyskiwania lub wszystkich planów odzyskiwania w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="a8a56-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="a8a56-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8a56-110">EXAMPLES</span></span>

### <span data-ttu-id="a8a56-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a8a56-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="a8a56-112">Pobiera plan odzyskiwania o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="a8a56-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="a8a56-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8a56-113">PARAMETERS</span></span>

### <span data-ttu-id="a8a56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a56-114">-DefaultProfile</span></span>
<span data-ttu-id="a8a56-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8a56-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a8a56-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a8a56-116">-FriendlyName</span></span>
<span data-ttu-id="a8a56-117">Określa przyjazną nazwę planu odzyskiwania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="a8a56-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="a8a56-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a8a56-118">-Name</span></span>
<span data-ttu-id="a8a56-119">Określa nazwę planu odzyskiwania, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="a8a56-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="a8a56-120">-Path</span><span class="sxs-lookup"><span data-stu-id="a8a56-120">-Path</span></span>
<span data-ttu-id="a8a56-121">Określa ścieżkę pliku, do którego to polecenie cmdlet zapisuje definicję JSON planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a8a56-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="a8a56-122">Definicję JSON można edytować w celu zmodyfikowania planu odzyskiwania i użycia w celu zaktualizowania planu odzyskiwania za pomocą polecenia cmdlet Update-AzRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8a56-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="a8a56-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a56-123">CommonParameters</span></span>
<span data-ttu-id="a8a56-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8a56-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a56-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8a56-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a56-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8a56-126">INPUTS</span></span>

### <span data-ttu-id="a8a56-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a8a56-127">None</span></span>

## <span data-ttu-id="a8a56-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8a56-128">OUTPUTS</span></span>

### <span data-ttu-id="a8a56-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8a56-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="a8a56-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8a56-130">NOTES</span></span>

## <span data-ttu-id="a8a56-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8a56-131">RELATED LINKS</span></span>

[<span data-ttu-id="a8a56-132">Nowe — AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8a56-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a8a56-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8a56-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a8a56-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8a56-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
