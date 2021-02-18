---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181563"
---
# <span data-ttu-id="e2d29-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="e2d29-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="e2d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2d29-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d29-103">Tworzy obiekt konfiguracji dla poświadczeń magazynu kluczy serwera SQL na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2d29-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="e2d29-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e2d29-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2d29-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e2d29-105">DESCRIPTION</span></span>

## <span data-ttu-id="e2d29-106">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e2d29-106">EXAMPLES</span></span>

## <span data-ttu-id="e2d29-107">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2d29-107">PARAMETERS</span></span>

### <span data-ttu-id="e2d29-108">— AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="e2d29-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="e2d29-109">Adres URL usługi magazynu kluczy platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e2d29-109">Azure Key Vault service URL</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d29-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="e2d29-110">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d29-111">— Włącz</span><span class="sxs-lookup"><span data-stu-id="e2d29-111">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d29-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d29-112">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d29-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e2d29-113">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d29-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="e2d29-114">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d29-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2d29-115">-Confirm</span></span>
<span data-ttu-id="e2d29-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e2d29-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d29-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d29-117">-WhatIf</span></span>
<span data-ttu-id="e2d29-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2d29-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2d29-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e2d29-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d29-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d29-120">CommonParameters</span></span>
<span data-ttu-id="e2d29-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2d29-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d29-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2d29-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d29-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2d29-123">INPUTS</span></span>

### <span data-ttu-id="e2d29-124">System.String</span><span class="sxs-lookup"><span data-stu-id="e2d29-124">System.String</span></span>

### <span data-ttu-id="e2d29-125">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e2d29-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e2d29-126">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="e2d29-126">System.Security.SecureString</span></span>

## <span data-ttu-id="e2d29-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2d29-127">OUTPUTS</span></span>

### <span data-ttu-id="e2d29-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="e2d29-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="e2d29-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e2d29-129">NOTES</span></span>

## <span data-ttu-id="e2d29-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2d29-130">RELATED LINKS</span></span>
