---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: c6d15769891f02a6c1be12a277e17ca2ccba107e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305677"
---
# <span data-ttu-id="5e17e-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="5e17e-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="5e17e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e17e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e17e-103">Próbuje włączyć Magazyn kluczy zarządzanych przez użytkownika w celu szyfrowania określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5e17e-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="5e17e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e17e-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e17e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5e17e-105">DESCRIPTION</span></span>
<span data-ttu-id="5e17e-106">Polecenie cmdlet **enable-AzDataLakeStoreKeyVault** usiłuje włączyć Magazyn kluczy zarządzanych przez użytkownika w celu szyfrowania określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5e17e-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="5e17e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e17e-107">EXAMPLES</span></span>

### <span data-ttu-id="5e17e-108">Przykład 1: Włączanie magazynu kluczy dla konta ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="5e17e-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="5e17e-109">To polecenie próbuje włączyć Magazyn kluczy zarządzanych przez użytkownika dla konta usługi Data Lake Store o nazwie ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="5e17e-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="5e17e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e17e-110">PARAMETERS</span></span>

### <span data-ttu-id="5e17e-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="5e17e-111">-Account</span></span>
<span data-ttu-id="5e17e-112">Konto usługi Data Lake Store umożliwiające włączenie magazynu kluczy zarządzanych przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="5e17e-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="5e17e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e17e-113">-DefaultProfile</span></span>
<span data-ttu-id="5e17e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5e17e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e17e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e17e-115">-ResourceGroupName</span></span>
<span data-ttu-id="5e17e-116">Nazwa grupy zasobów skojarzonej z kontem.</span><span class="sxs-lookup"><span data-stu-id="5e17e-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="5e17e-117">Jeśli nie określono, zostanie wykryta próba.</span><span class="sxs-lookup"><span data-stu-id="5e17e-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="5e17e-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e17e-118">-Confirm</span></span>
<span data-ttu-id="5e17e-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e17e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e17e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e17e-120">-WhatIf</span></span>
<span data-ttu-id="5e17e-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e17e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e17e-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e17e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e17e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e17e-123">CommonParameters</span></span>
<span data-ttu-id="5e17e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e17e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e17e-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e17e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e17e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e17e-126">INPUTS</span></span>

### <span data-ttu-id="5e17e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5e17e-127">System.String</span></span>

## <span data-ttu-id="5e17e-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e17e-128">OUTPUTS</span></span>

### <span data-ttu-id="5e17e-129">System. void</span><span class="sxs-lookup"><span data-stu-id="5e17e-129">System.Void</span></span>

## <span data-ttu-id="5e17e-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e17e-130">NOTES</span></span>

## <span data-ttu-id="5e17e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e17e-131">RELATED LINKS</span></span>

[<span data-ttu-id="5e17e-132">Nowe — AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5e17e-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5e17e-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5e17e-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

