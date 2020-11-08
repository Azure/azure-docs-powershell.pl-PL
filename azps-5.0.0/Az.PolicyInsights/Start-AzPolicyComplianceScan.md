---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225834"
---
# <span data-ttu-id="b4737-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="b4737-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="b4737-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4737-102">SYNOPSIS</span></span>
<span data-ttu-id="b4737-103">Wyzwala ocenę zgodności zasad dla wszystkich zasobów w subskrypcji lub grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4737-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="b4737-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4737-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4737-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b4737-105">DESCRIPTION</span></span>
<span data-ttu-id="b4737-106">Polecenie cmdlet **Start-AzPolicyComplianceScan** rozpoczyna ocenę zgodności zasad dla subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4737-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="b4737-107">Stan zgodności wszystkich zasobów w tym zakresie będzie oceniany względem wszystkich przypisanych zasad.</span><span class="sxs-lookup"><span data-stu-id="b4737-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="b4737-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4737-108">EXAMPLES</span></span>

### <span data-ttu-id="b4737-109">Przykład 1. Rozpoczynanie skanowania zgodności w zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b4737-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="b4737-110">To polecenie rozpoczyna ocenę zgodności z zasadami dotyczącymi aktywnej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b4737-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="b4737-111">Przykład 2: Rozpoczynanie skanowania zgodności w zakresie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b4737-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="b4737-112">To polecenie rozpoczyna ocenę zgodności zasad dla grupy zasobów "myRG" w aktywnej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b4737-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="b4737-113">Przykład 3: Rozpoczynanie skanowania zgodności i oczekiwanie na ukończenie pracy w tle</span><span class="sxs-lookup"><span data-stu-id="b4737-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="b4737-114">To polecenie rozpoczyna ocenę zgodności z zasadami dotyczącymi aktywnej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b4737-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="b4737-115">Przestanie on czekać na ukończenie skanowania.</span><span class="sxs-lookup"><span data-stu-id="b4737-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="b4737-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4737-116">PARAMETERS</span></span>

### <span data-ttu-id="b4737-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4737-117">-AsJob</span></span>
<span data-ttu-id="b4737-118">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="b4737-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b4737-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4737-119">-DefaultProfile</span></span>
<span data-ttu-id="b4737-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4737-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4737-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4737-121">-PassThru</span></span>
<span data-ttu-id="b4737-122">Zwraca wartość true, jeśli polecenie zostało pomyślnie ukończone.</span><span class="sxs-lookup"><span data-stu-id="b4737-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="b4737-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4737-123">-ResourceGroupName</span></span>
<span data-ttu-id="b4737-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4737-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4737-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4737-125">-Confirm</span></span>
<span data-ttu-id="b4737-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4737-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4737-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4737-127">-WhatIf</span></span>
<span data-ttu-id="b4737-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4737-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4737-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4737-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4737-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4737-130">CommonParameters</span></span>
<span data-ttu-id="b4737-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4737-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4737-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4737-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4737-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4737-133">INPUTS</span></span>

### <span data-ttu-id="b4737-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b4737-134">System.String</span></span>

## <span data-ttu-id="b4737-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4737-135">OUTPUTS</span></span>

### <span data-ttu-id="b4737-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4737-136">System.Boolean</span></span>

## <span data-ttu-id="b4737-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4737-137">NOTES</span></span>

## <span data-ttu-id="b4737-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4737-138">RELATED LINKS</span></span>
