---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 10a441cd1354b75a13b429c4375e7bc3fba72244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224242"
---
# <span data-ttu-id="9bef5-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="9bef5-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="9bef5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bef5-102">SYNOPSIS</span></span>
<span data-ttu-id="9bef5-103">Zaktualizuj stan magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9bef5-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="9bef5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bef5-104">SYNTAX</span></span>

### <span data-ttu-id="9bef5-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9bef5-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bef5-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bef5-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bef5-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bef5-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bef5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9bef5-108">DESCRIPTION</span></span>
<span data-ttu-id="9bef5-109">To polecenie cmdlet aktualizuje stan magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9bef5-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="9bef5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bef5-110">EXAMPLES</span></span>

### <span data-ttu-id="9bef5-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9bef5-111">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="9bef5-112">Włącza ochronę przed przeczyszczaniem za pomocą składni połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="9bef5-112">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="9bef5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bef5-113">PARAMETERS</span></span>

### <span data-ttu-id="9bef5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bef5-114">-DefaultProfile</span></span>
<span data-ttu-id="9bef5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bef5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bef5-116">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="9bef5-116">-EnablePurgeProtection</span></span>
<span data-ttu-id="9bef5-117">Włącz funkcję zabezpieczenia przed przeczyszczaniem dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="9bef5-117">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="9bef5-118">Po włączeniu tej możliwości nie można jej wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="9bef5-118">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="9bef5-119">Funkcja ta wymaga włączenia Soft-Delete.</span><span class="sxs-lookup"><span data-stu-id="9bef5-119">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="9bef5-120">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="9bef5-120">-EnableRbacAuthorization</span></span>
<span data-ttu-id="9bef5-121">Włącz lub Wyłącz ten magazyn kluczy, aby autoryzować akcje danych według kontroli dostępu opartej na rolach (RBAC).</span><span class="sxs-lookup"><span data-stu-id="9bef5-121">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bef5-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9bef5-122">-InputObject</span></span>
<span data-ttu-id="9bef5-123">Obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="9bef5-123">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bef5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bef5-124">-ResourceGroupName</span></span>
<span data-ttu-id="9bef5-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9bef5-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bef5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bef5-126">-ResourceId</span></span>
<span data-ttu-id="9bef5-127">Identyfikator zasobu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="9bef5-127">Resource ID of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bef5-128">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="9bef5-128">-VaultName</span></span>
<span data-ttu-id="9bef5-129">Nazwa magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="9bef5-129">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bef5-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9bef5-130">-Confirm</span></span>
<span data-ttu-id="9bef5-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bef5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bef5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bef5-132">-WhatIf</span></span>
<span data-ttu-id="9bef5-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bef5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bef5-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9bef5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bef5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bef5-135">CommonParameters</span></span>
<span data-ttu-id="9bef5-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bef5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bef5-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bef5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bef5-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bef5-138">INPUTS</span></span>

### <span data-ttu-id="9bef5-139">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9bef5-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="9bef5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9bef5-140">System.String</span></span>

## <span data-ttu-id="9bef5-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bef5-141">OUTPUTS</span></span>

### <span data-ttu-id="9bef5-142">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9bef5-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="9bef5-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bef5-143">NOTES</span></span>

## <span data-ttu-id="9bef5-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bef5-144">RELATED LINKS</span></span>
