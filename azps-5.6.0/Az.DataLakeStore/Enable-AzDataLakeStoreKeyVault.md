---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: 2b4b225ca050e3efedb1de1371006a4ffdb87587
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952673"
---
# <span data-ttu-id="948ca-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="948ca-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="948ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="948ca-102">SYNOPSIS</span></span>
<span data-ttu-id="948ca-103">Próbuje włączyć zarządzany przez użytkownika magazyn kluczy w celu szyfrowania określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="948ca-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="948ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="948ca-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="948ca-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="948ca-105">DESCRIPTION</span></span>
<span data-ttu-id="948ca-106">Polecenie **cmdlet Enable-AzDataLakeStoreKeyVault** próbuje włączyć zarządzany przez użytkownika magazyn kluczy do szyfrowania określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="948ca-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="948ca-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="948ca-107">EXAMPLES</span></span>

### <span data-ttu-id="948ca-108">Przykład 1. Włączanie magazynu kluczy dla konta ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="948ca-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="948ca-109">To polecenie próbuje włączyć zarządzany przez użytkownika magazyn kluczy dla konta Data Lake Store o nazwie ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="948ca-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="948ca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="948ca-110">PARAMETERS</span></span>

### <span data-ttu-id="948ca-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="948ca-111">-Account</span></span>
<span data-ttu-id="948ca-112">Konto usługi Data Lake Store w celu umożliwienia użytkownikowi zarządzanego magazynu kluczy dla</span><span class="sxs-lookup"><span data-stu-id="948ca-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948ca-113">-DefaultProfile</span></span>
<span data-ttu-id="948ca-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="948ca-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="948ca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="948ca-115">-ResourceGroupName</span></span>
<span data-ttu-id="948ca-116">Nazwa grupy zasobów skojarzonej z kontem.</span><span class="sxs-lookup"><span data-stu-id="948ca-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="948ca-117">Jeśli nie określono, spróbuje on wykryć.</span><span class="sxs-lookup"><span data-stu-id="948ca-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="948ca-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="948ca-118">-Confirm</span></span>
<span data-ttu-id="948ca-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="948ca-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="948ca-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="948ca-120">-WhatIf</span></span>
<span data-ttu-id="948ca-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="948ca-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="948ca-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="948ca-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="948ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948ca-123">CommonParameters</span></span>
<span data-ttu-id="948ca-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="948ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948ca-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948ca-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948ca-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="948ca-126">INPUTS</span></span>

### <span data-ttu-id="948ca-127">System.String</span><span class="sxs-lookup"><span data-stu-id="948ca-127">System.String</span></span>

## <span data-ttu-id="948ca-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="948ca-128">OUTPUTS</span></span>

### <span data-ttu-id="948ca-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="948ca-129">System.Void</span></span>

## <span data-ttu-id="948ca-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="948ca-130">NOTES</span></span>

## <span data-ttu-id="948ca-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="948ca-131">RELATED LINKS</span></span>

[<span data-ttu-id="948ca-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="948ca-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="948ca-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="948ca-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

