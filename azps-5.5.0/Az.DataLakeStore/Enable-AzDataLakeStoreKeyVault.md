---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: c6d15769891f02a6c1be12a277e17ca2ccba107e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243890"
---
# <span data-ttu-id="a71b1-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="a71b1-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="a71b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a71b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a71b1-103">Próbuje włączyć zarządzany przez użytkownika magazyn kluczy w celu szyfrowania określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a71b1-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="a71b1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a71b1-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a71b1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a71b1-105">DESCRIPTION</span></span>
<span data-ttu-id="a71b1-106">Polecenie **cmdlet Enable-AzDataLakeStoreKeyVault** próbuje włączyć zarządzany przez użytkownika magazyn kluczy do szyfrowania określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a71b1-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="a71b1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a71b1-107">EXAMPLES</span></span>

### <span data-ttu-id="a71b1-108">Przykład 1. Włączanie magazynu kluczy dla konta ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="a71b1-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="a71b1-109">To polecenie próbuje włączyć zarządzany przez użytkownika magazyn kluczy dla konta Data Lake Store o nazwie ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="a71b1-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="a71b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a71b1-110">PARAMETERS</span></span>

### <span data-ttu-id="a71b1-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="a71b1-111">-Account</span></span>
<span data-ttu-id="a71b1-112">Konto usługi Data Lake Store w celu umożliwienia użytkownikowi zarządzanego magazynu kluczy dla</span><span class="sxs-lookup"><span data-stu-id="a71b1-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="a71b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a71b1-113">-DefaultProfile</span></span>
<span data-ttu-id="a71b1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a71b1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a71b1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a71b1-115">-ResourceGroupName</span></span>
<span data-ttu-id="a71b1-116">Nazwa grupy zasobów skojarzonej z kontem.</span><span class="sxs-lookup"><span data-stu-id="a71b1-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="a71b1-117">Jeśli nie określono, spróbuje on wykryć.</span><span class="sxs-lookup"><span data-stu-id="a71b1-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="a71b1-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a71b1-118">-Confirm</span></span>
<span data-ttu-id="a71b1-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a71b1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a71b1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a71b1-120">-WhatIf</span></span>
<span data-ttu-id="a71b1-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a71b1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a71b1-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a71b1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a71b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a71b1-123">CommonParameters</span></span>
<span data-ttu-id="a71b1-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a71b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a71b1-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a71b1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a71b1-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a71b1-126">INPUTS</span></span>

### <span data-ttu-id="a71b1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a71b1-127">System.String</span></span>

## <span data-ttu-id="a71b1-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a71b1-128">OUTPUTS</span></span>

### <span data-ttu-id="a71b1-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="a71b1-129">System.Void</span></span>

## <span data-ttu-id="a71b1-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a71b1-130">NOTES</span></span>

## <span data-ttu-id="a71b1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a71b1-131">RELATED LINKS</span></span>

[<span data-ttu-id="a71b1-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a71b1-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="a71b1-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a71b1-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

