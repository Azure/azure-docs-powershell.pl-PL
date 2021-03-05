---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 30bdfc03efd59b53cfed17b426b2b2411fb76d86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007089"
---
# <span data-ttu-id="964c8-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="964c8-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="964c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="964c8-102">SYNOPSIS</span></span>
<span data-ttu-id="964c8-103">Tworzy obiekt konfiguracji dla poświadczeń magazynu kluczy serwera SQL na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="964c8-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="964c8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="964c8-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="964c8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="964c8-105">DESCRIPTION</span></span>

## <span data-ttu-id="964c8-106">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="964c8-106">EXAMPLES</span></span>

## <span data-ttu-id="964c8-107">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="964c8-107">PARAMETERS</span></span>

### <span data-ttu-id="964c8-108">— AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="964c8-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="964c8-109">Adres URL usługi magazynu kluczy platformy Azure</span><span class="sxs-lookup"><span data-stu-id="964c8-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="964c8-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="964c8-110">-CredentialName</span></span>
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

### <span data-ttu-id="964c8-111">— Włącz</span><span class="sxs-lookup"><span data-stu-id="964c8-111">-Enable</span></span>
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

### <span data-ttu-id="964c8-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="964c8-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="964c8-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="964c8-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="964c8-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="964c8-114">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="964c8-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="964c8-115">-Confirm</span></span>
<span data-ttu-id="964c8-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="964c8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="964c8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="964c8-117">-WhatIf</span></span>
<span data-ttu-id="964c8-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="964c8-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="964c8-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="964c8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="964c8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964c8-120">CommonParameters</span></span>
<span data-ttu-id="964c8-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="964c8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964c8-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="964c8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964c8-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="964c8-123">INPUTS</span></span>

### <span data-ttu-id="964c8-124">System.String</span><span class="sxs-lookup"><span data-stu-id="964c8-124">System.String</span></span>

### <span data-ttu-id="964c8-125">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="964c8-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="964c8-126">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="964c8-126">System.Security.SecureString</span></span>

## <span data-ttu-id="964c8-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="964c8-127">OUTPUTS</span></span>

### <span data-ttu-id="964c8-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="964c8-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="964c8-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="964c8-129">NOTES</span></span>

## <span data-ttu-id="964c8-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="964c8-130">RELATED LINKS</span></span>
