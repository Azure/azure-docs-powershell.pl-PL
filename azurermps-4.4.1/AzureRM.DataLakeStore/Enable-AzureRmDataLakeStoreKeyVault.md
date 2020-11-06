---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: a168b48089052ed8daa764407254d04084ece771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527605"
---
# <span data-ttu-id="64bce-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="64bce-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="64bce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64bce-102">SYNOPSIS</span></span>
<span data-ttu-id="64bce-103">Próbuje włączyć Magazyn kluczy zarządzanych przez użytkownika w celu szyfrowania określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="64bce-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64bce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64bce-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64bce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64bce-105">DESCRIPTION</span></span>
<span data-ttu-id="64bce-106">Polecenie cmdlet **enable-AzureRmDataLakeStoreKeyVault** usiłuje włączyć Magazyn kluczy zarządzanych przez użytkownika w celu szyfrowania określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="64bce-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="64bce-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64bce-107">EXAMPLES</span></span>

### <span data-ttu-id="64bce-108">Przykład 1: Włączanie magazynu kluczy dla konta ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="64bce-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="64bce-109">To polecenie próbuje włączyć Magazyn kluczy zarządzanych przez użytkownika dla konta usługi Data Lake Store o nazwie ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="64bce-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="64bce-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64bce-110">PARAMETERS</span></span>

### <span data-ttu-id="64bce-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="64bce-111">-Account</span></span>
<span data-ttu-id="64bce-112">Konto usługi Data Lake Store umożliwiające włączenie magazynu kluczy zarządzanych przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="64bce-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="64bce-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64bce-113">-ResourceGroupName</span></span>
<span data-ttu-id="64bce-114">Nazwa grupy zasobów skojarzonej z kontem.</span><span class="sxs-lookup"><span data-stu-id="64bce-114">Name of resource group associated with the account.</span></span> <span data-ttu-id="64bce-115">Jeśli nie określono, zostanie wykryta próba.</span><span class="sxs-lookup"><span data-stu-id="64bce-115">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="64bce-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64bce-116">-Confirm</span></span>
<span data-ttu-id="64bce-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64bce-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64bce-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64bce-118">-WhatIf</span></span>
<span data-ttu-id="64bce-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64bce-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64bce-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64bce-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64bce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bce-121">-DefaultProfile</span></span>
<span data-ttu-id="64bce-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64bce-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64bce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bce-123">CommonParameters</span></span>
<span data-ttu-id="64bce-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64bce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bce-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64bce-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bce-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64bce-126">INPUTS</span></span>

### <span data-ttu-id="64bce-127">System. String</span><span class="sxs-lookup"><span data-stu-id="64bce-127">System.String</span></span>

## <span data-ttu-id="64bce-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64bce-128">OUTPUTS</span></span>

## <span data-ttu-id="64bce-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64bce-129">NOTES</span></span>

## <span data-ttu-id="64bce-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64bce-130">RELATED LINKS</span></span>

[<span data-ttu-id="64bce-131">Nowe — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="64bce-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="64bce-132">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="64bce-132">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

