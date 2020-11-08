---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225533"
---
# <span data-ttu-id="a9fec-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a9fec-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="a9fec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9fec-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fec-103">Pobiera plan odzyskiwania lub wszystkie plany odzyskiwania w magazynie usług Recovery Services</span><span class="sxs-lookup"><span data-stu-id="a9fec-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="a9fec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9fec-104">SYNTAX</span></span>

### <span data-ttu-id="a9fec-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a9fec-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9fec-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a9fec-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9fec-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a9fec-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9fec-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9fec-108">DESCRIPTION</span></span>
<span data-ttu-id="a9fec-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan** pobiera szczegóły określonego planu odzyskiwania lub wszystkich planów odzyskiwania w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="a9fec-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="a9fec-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9fec-110">EXAMPLES</span></span>

### <span data-ttu-id="a9fec-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9fec-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="a9fec-112">Pobiera plan odzyskiwania o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="a9fec-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="a9fec-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9fec-113">PARAMETERS</span></span>

### <span data-ttu-id="a9fec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fec-114">-DefaultProfile</span></span>
<span data-ttu-id="a9fec-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9fec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a9fec-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a9fec-116">-FriendlyName</span></span>
<span data-ttu-id="a9fec-117">Określa przyjazną nazwę planu odzyskiwania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="a9fec-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="a9fec-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9fec-118">-Name</span></span>
<span data-ttu-id="a9fec-119">Określa nazwę planu odzyskiwania, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="a9fec-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="a9fec-120">-Path</span><span class="sxs-lookup"><span data-stu-id="a9fec-120">-Path</span></span>
<span data-ttu-id="a9fec-121">Określa ścieżkę pliku, do którego to polecenie cmdlet zapisuje definicję JSON planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a9fec-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="a9fec-122">Definicję JSON można edytować w celu zmodyfikowania planu odzyskiwania i użycia w celu zaktualizowania planu odzyskiwania za pomocą polecenia cmdlet Update-AzRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a9fec-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="a9fec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fec-123">CommonParameters</span></span>
<span data-ttu-id="a9fec-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9fec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fec-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9fec-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fec-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9fec-126">INPUTS</span></span>

### <span data-ttu-id="a9fec-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a9fec-127">None</span></span>

## <span data-ttu-id="a9fec-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9fec-128">OUTPUTS</span></span>

### <span data-ttu-id="a9fec-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a9fec-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="a9fec-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9fec-130">NOTES</span></span>

## <span data-ttu-id="a9fec-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9fec-131">RELATED LINKS</span></span>

[<span data-ttu-id="a9fec-132">Nowe — AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a9fec-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a9fec-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a9fec-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a9fec-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a9fec-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
