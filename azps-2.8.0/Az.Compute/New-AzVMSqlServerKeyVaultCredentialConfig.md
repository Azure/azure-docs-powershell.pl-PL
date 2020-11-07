---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 5d8f67de6b6bbe08a34dad279674b29befaa161c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706317"
---
# <span data-ttu-id="61aaa-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="61aaa-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="61aaa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="61aaa-103">Tworzy obiekt konfiguracji dla poświadczenia magazynu kluczy programu SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="61aaa-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="61aaa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61aaa-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61aaa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="61aaa-105">DESCRIPTION</span></span>

## <span data-ttu-id="61aaa-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61aaa-106">EXAMPLES</span></span>

## <span data-ttu-id="61aaa-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61aaa-107">PARAMETERS</span></span>

### <span data-ttu-id="61aaa-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="61aaa-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="61aaa-109">Adres URL usługi Magazyn kluczy Azure</span><span class="sxs-lookup"><span data-stu-id="61aaa-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="61aaa-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="61aaa-110">-CredentialName</span></span>
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

### <span data-ttu-id="61aaa-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="61aaa-111">-Enable</span></span>
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

### <span data-ttu-id="61aaa-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61aaa-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="61aaa-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="61aaa-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="61aaa-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="61aaa-114">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="61aaa-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61aaa-115">-Confirm</span></span>
<span data-ttu-id="61aaa-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61aaa-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61aaa-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61aaa-117">-WhatIf</span></span>
<span data-ttu-id="61aaa-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61aaa-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61aaa-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61aaa-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61aaa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61aaa-120">CommonParameters</span></span>
<span data-ttu-id="61aaa-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61aaa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61aaa-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61aaa-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61aaa-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61aaa-123">INPUTS</span></span>

### <span data-ttu-id="61aaa-124">System. String</span><span class="sxs-lookup"><span data-stu-id="61aaa-124">System.String</span></span>

### <span data-ttu-id="61aaa-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="61aaa-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="61aaa-126">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="61aaa-126">System.Security.SecureString</span></span>

## <span data-ttu-id="61aaa-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61aaa-127">OUTPUTS</span></span>

### <span data-ttu-id="61aaa-128">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="61aaa-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="61aaa-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61aaa-129">NOTES</span></span>

## <span data-ttu-id="61aaa-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61aaa-130">RELATED LINKS</span></span>